<properties
    pageTitle="VM boot error Recovery Console"
    description="Virtual machine failed to boot with error code Recovery Console."
    infoBubbleText="A boot error 'Recovery Console' has beeen detected. Press Ctrl+Alt+Del to restart' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="BootError-RECOVERY_CONSOLE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operating system.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error message **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. [Stop the VM and create a snapshot](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
2. Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
3. Disable the policy or disable the service which startup account is causing the deadlock:

    1. Open the registry editor with `REGEDIT`
    2. Highlight the key `HKEY_LOCAL_MACHINE` and select File - Load Hive from the menu
    3. Browse to the file `\windows\system32\config\BROKENSOFTWARE` on the data disk that is the copy of the affected Machine
    4. Navigate to `HKLM\BROKENSOFTWARE\?Policies\Microsoft\Windows\System` verify if the CleanupProfile key exists. If it does, run  `REG DELETE "HKLM\BROKENSOFTWARE\?Policies\Microsoft\Windows\System" /v CleanupProfiles /f`. If the key does NOT exist, unload the BROKENSOFTWARE hive with `reg unload HKLM\BROKENSOFTWARE`
    5. If this issue was fixed by disabling this policy locally, avoid using the CleanupProfiles policy and use this method to perform the profile cleanup: `Machine\Admin Templates\System\User Profiles\Delete user profiles older than a specified number of days on system restart`

4. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition. The Windows partition contains a folder named "Windows," and this partition is larger than the others. The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.

    1. As administrator, run `bcdedit /store [Boot partition]:\boot\bcd /enum` and copy the Windows Boot Loader identifier. The identifier is a 32-character code in the format xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.
    2. Repair the Boot Configuration data by running the following command lines, using actual values. "Windows partition" is the partition that contains a folder named "Windows, "Boot partition" is the partition that contains a hidden system folder named "Boot, and "Identifier" is the identifier of Windows Boot Loader you found in the previous step:

```
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```

 5. Run [Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). When it will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
