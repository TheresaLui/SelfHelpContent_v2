<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to process Windows Updates during installation"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="OSStartUp-WINDOWS_COULD_NOT_COMPLETE_INSTALLATION"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operating system.
<!--/issueDescription-->

## **Recommended Steps**

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code 'An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart'. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

1.  [Stop the VM and create a snapshot](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
2.  Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/blob/master/VMRecovery/ResourceManager/New-AzureRMRescueVM.ps1)
3.  Run cmd.exe as administrator and display the current boot setup information with this command:

    ```
    bcdedit /store <drive letter>:\boot\bcd /enum
    ```

    1.  In the output of the preceding command, the Windows Boot Manager is the partition with identifier bootmgr, but the default property values and display order are not shown. In the same output, find the identifier of the Windows Boot Loader, whose path value is \Windows\system32\winload.exe. Use the identifier in the following commands, to determine the default property values and the display order.

        ```
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} default {<IDENTIFIER FROM THE BOOT LOADER>}
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} displayorder {<IDENTIFIER FROM THE BOOT LOADER>}
        ```

    2.  Run the following commands to verify everything is in place:

        ```
        C:\Users\azureadmin>bcdedit /store f:\boot\bcd /set {bootmgr} displayorder {05d0826e-19a2-4380-968f-4b45f971812d}
        The element data type specified is not recognized, or does not apply to the specified entry.
        Run "bcdedit /?" for command line assistance.
        ```

    3.  If you get the 'Element not found.' error then the entire {bootmgr} is gone. To recreate it then run:

        ```
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /create {bootmgr}
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} description "Windows Boot Manager"
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} locale en-us
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} inherit {globalsettings}
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} displayorder {<IDENTIFIER FROM THE BOOT LOADER>}
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} default {<IDENTIFIER FROM THE BOOT LOADER>}
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} timeout 30
        ```

4.  Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition. The Windows partition contains a folder named "Windows," and this partition is larger than the others. The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.

    1.  As administrator, run `bcdedit /store [Boot partition]:\boot\bcd /enum` and copy the Windows Boot Loader identifier. The identifier is a 32-character code in the format xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. 
    2.  Repair the Boot Configuration data by running the following command lines, using actual values. "Windows partition" is the partition that contains a folder named "Windows, "Boot partition" is the partition that contains a hidden system folder named "Boot, and "Identifier" is the identifier of Windows Boot Loader you found in the previous step:

        ```
        bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
        bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
        bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
        bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
        bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
        bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
        bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
        ```

5.  [Run Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). It will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
