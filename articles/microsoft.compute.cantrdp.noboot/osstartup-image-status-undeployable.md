<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot because it found the OS to be unhealthy and the automatic system recovery tried to fix it."
    infoBubbleText="A boot error 'An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart' has been found for your virtual machine."
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
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
 
# VM Boot Error
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because we could not find an operating system.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VmSerialConsoleLogBlade.id.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart**.  This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. [Stop the VM and create a snapshot](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager)
2. Run [New-AzureRMRescueVM.ps1](https://github.com/Azure/azure-support-scripts/blob/master/VMRecovery/ResourceManager/New-AzureRMRescueVM.ps1)
3. Verify the OS partition that holds the BCD store for the disk is marked as active:

    1. Open an elevated command prompt and open `diskpart`
    2. List the disks on the system with `list disk`, check for added disks, and use `sel disk 1` to select the new disk
    3. List all the partitions on the disk using `list partition` and select the partition to check with `sel <PARTITION ID>`. Typically, System Managed partitions are around 350Mb in size.
    4. Check the status of the partition to verify that it's Active using `detail partition`
    5. Check for the "Active" flag. If the partition is not active, change the state with `active`
    6. To validate the changes were done properly, re-run `detail partition`. Type `Exit` when ready.

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

5. [Run Restore-AzureRMOriginalVM.ps1](https://github.com/Azure/azure-support-scripts/tree/master/VMRecovery/ResourceManager). This will create a PowerShell script, Restore_.ps1, that you will run later to swap the problem VM's OS disk back to the problem VM.
