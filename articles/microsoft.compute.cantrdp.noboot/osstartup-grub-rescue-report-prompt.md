<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it couldn't finitialize Windows"
    infoBubbleText="A boot error 'OSStartUp--IMAGE_STATUS_UNDEPLOYABLE' has been found for your virtual machine."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="OSStartUp--IMAGE_STATUS_UNDEPLOYABLE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operating system.

You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**
To remediate this problem, we recommend taking the following steps:

1. [Stop the VM and create a snapshot.](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

2. <!--/Phase 1-->Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager).

3. <!--/Phase 2 Mitigation--> The inage of your VM is corrupted. To address this, you will need to follow the steps in this article: [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/prepare-for-upload-vhd-image?toc=%2Fazure%2Fvirtual-machines%2Fwindows%2Ftoc.json)

4.  Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition.
    * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
    * The Boot partition contains
    a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB

  a. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step

      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```

   b. Repair the Boot Configuration data by running the following command lines. You must replace these placeholders by the actual values:
  * "Windows partition" is the partition that contains a folder named "Windows."
  * "Boot partition" is the partition that contains a hidden system folder named "Boot."
  * "Identifier" is the identifier of Windows Boot Loader you found in the previous step.

        ```
          bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
          bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
          bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
          bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
          bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
          bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
          bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
        ```

5. <!--/Phase 3--> Run [Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). When it will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
