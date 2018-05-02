<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with error code 0xC0000359"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani"
displayOrder=""
articleId="VMCannotRDP_A139226A-AD29-487A-80BE-4BD8CE6095CC"
diagnosticScenario="booterror"
selfHelpType="diagnostics"
supportTopicIds="32411835"
resourceTags="windows"
productPesIds="14749"
cloudEnvironments="public"
/>

# VM boot error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
Microsoft Azure has concluded an investigation of your Virtual Machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname-->. We identified that your VM is currently in an inaccessible state because windows failed to boot with error code **0xc0000359**. The issue occurs because the binary file is the 32-bit version and it needs to be replaced by the 64-bit version.<br>
<!--/issueDescription-->

## **Recommended Steps**
To fix the issue, either replace the file from the C:\windows\WinSxS folder on the same machine or from another working VM with the same OS and Patch level as this machine following these troubleshooting steps.

1. Please make a note of the File name and the path from the screenshot.
2. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the Keep the disks option when you do this.
3. Before proceeding further save a copy of the OS disk, this will help in case of a rollback for recovery, see [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy)
4. Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
5. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
6. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is the Boot partition and the Windows partition.
  * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
  * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB
7. In the attached OS Disk, browse to the file path noted in Step 1 and rename the file as [BINARY.SYS].OLD.
8. Now from an elevated command prompt, locate the volume holding your Windows directory, browse to \windows\winsxs and search for the binary displayed on your screenshot. The below commands will give you all the different versions file on the machine.
```
  dir [binary name without the extension]* /s
```
9. Choose the latest of the list and proceed to copy it to the windows\system32 folder path on the attached OS disk.
```
  copy [drive]:\Windows\WinSxS\[directory_where_file_is]\[binary_with_extension] [drive]:\Windows\System32\Drivers\   
```
10. If another file cannot be found, then look for a machine with the same OS version and same patch level (if possible), locate the binary and replace the missing binary on the affected machine.
11. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-create-vm-specialized)
