<properties
pageTitle="VM in reboot loop"
description="Virtual machine failed to boot with error code 0xC00002E3"
infoBubbleText="VM is in a reboot loop. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani, timbasham, jasonbandrew"
ms.author="ramakk, tibasham, v-jasoan"
displayOrder=""
articleId="VMCannotRDP_FFE84A13-177A-4524-8BD7-3D13E8048893"
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

We have have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname-->  is currently in an inaccessible state as it is in a reboot loop with an error code **0xC00002e3**. The issue occurs when the SAM registry hive is missing or corrupt.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To fix the issue, either replace the file from the C:\windows\WinSxS folder on the same machine or from another working VM with the same OS and Patch level as this machine following these troubleshooting steps.

1. Please make a note of the File name and the path from the screenshot.
2. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the Keep the disks option when you do this.
3. Before proceeding further save a copy of the OS disk, this will help in case of a rollback for recovery, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
4. Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
5. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
6. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition.
  * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
  * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB
7. Browse up to the folder \windows\system32\config and check if the file SAM exist, if it does rename it to SAM.CORRUPT.
8. In case you have a backup of the Disk or a System backup taken before the VM ran into this issue, please check if SAM file exists in \windows\system32\config.
9. If SAM file exists in the backup, replace/copy the file to the affected machine’s OS Disk \windows\system32\config folder.
10. In cases there are no backups, on the affected disk copy the file from \windows\system32\config\regback\SAM to \windows\system32\config\.
11. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-create-vm-specialized)
