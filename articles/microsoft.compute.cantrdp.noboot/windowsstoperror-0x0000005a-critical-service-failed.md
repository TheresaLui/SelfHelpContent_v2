<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot due to Error 0x0000005A-CRITICAL_SERVICE_FAILED."
    infoBubbleText="A boot error 'CRITICAL_PROCESS_FAILED' has been found for your virtual machine. The next step is to restart your VM."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="jasonbandrew"
    ms.author="v-jasoan"
    displayOrder=""
    articleId="WindowsStopError-0x0000005A-CRITICAL_SERVICE_FAILED"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax"
	ownershipId="Compute_ComputePlatform"
/>

# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operation system.

Use the Boot Diagnostics Screenshot to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**

1. [Stop the VM and create a snapshot](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
2. Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/blob/master/VMRecovery/ResourceManager/New-AzureRMRescueVM.ps1)
3. Follow the directions [CRITICAL SERVICE FAILED" on blue screen when booting an Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-critical-service-failed-boot-error).
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

5. [Run Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). When it will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
