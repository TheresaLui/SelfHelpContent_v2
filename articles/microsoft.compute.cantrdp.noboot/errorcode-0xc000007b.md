<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with error code 0xc000007b"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani, timbasham, jasonbandrew"
ms.author="ramakk, tibasham, v-jasoan"
displayOrder=""
articleId="VMCannotRDP_D49207E5-874F-4731-B42C-354D8F386A47"
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
We have have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> in an inaccessible state because windows failed to boot with error code **0xc000007b**. The operating system couldn’t be loaded because a critical system driver is corrupt.

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.
<!--/issueDescription-->

## **Recommended Steps**
To fix the issue, either replace the file from the C:\windows\WinSxS folder on the same machine or from another working VM with the same OS and Patch level as this machine following these troubleshooting steps.

1. Make a note of the File name and the path from the screenshot
2. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the Keep the disks option when you do this.
3. [Save a copy of the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/vhd-copy)
4. [Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM)](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal)
5. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned
6. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition. The Windows partition contains a folder named "Windows," and this partition is larger than the others. The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.
7. In the attached OS Disk, browse to the file path noted in Step 1 and rename the file as `[BINARY.SYS].OLD`
8. From an elevated command prompt, locate the volume holding your Windows directory, browse to \windows\winsxs and search for the binary displayed on your screenshot with `dir [binary name without the extension]* /s`
9. Choose the latest of the list and proceed to copy it to the windows\system32 folder path on the attached OS disk with `copy [drive]:\Windows\WinSxS\[directory_where_file_is]\[binary_with_extension] [drive]:\Windows\System32\Drivers\`
10. If another file cannot be found, then look for a machine with the same OS version and same patch level (if possible), locate the binary and replace the corrupt binary on the affected machine.
11. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized).
