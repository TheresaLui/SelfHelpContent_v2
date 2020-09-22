<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with error code 0xc0000001"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani, timbasham, jasonbandrew"
ms.author="ramakk, tibasham, v-jasoan"
displayOrder=""
articleId="VMCannotRDP-BootError-0xc0000001-BootBCD"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error
<!--issueDescription-->

We have have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because windows failed to boot with error code **0xc0000001**. The issue occurs when a device that doesn't exist is specified in the boot configuration data (BCD).

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To fix the BCD store, follow the troubleshooting steps indicated below:

1. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the "Keep the disks" option when you do this.
2. Before proceeding further, [save a copy of the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/vhd-copy)
3. [Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM)](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal)
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned
5. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition. The Windows partition contains a folder named "Windows," and this partition is larger than the others. The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB. 
6. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step: `bcdedit /store [Boot partition]:\boot\bcd /enum`
7. Repair the Boot Configuration data by running the following command lines. You must replace these placeholders by the actual values:
  
  ```
  bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} device partition=[boot partition]:
  bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} integrityservices enable
  bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} device partition=[Windows partition]:
  bcdedit /store [Boot partition]:\boot\bcd /set {[Identifier]} integrityservices enable
  bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} recoveryenabled Off
  bcdedit /store [Boot partition]:\boot\bcd /set {[identifier]} osdevice partition=[Windows partition]:
  bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
  ```

8. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized).
