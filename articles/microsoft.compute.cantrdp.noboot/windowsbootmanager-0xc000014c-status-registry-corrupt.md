<properties
    pageTitle="VM boot error"
    description="Virtual machine failed to boot with error *0xC000014C*"
    infoBubbleText="A boot error has been found. See details on the right."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="timbasham"
    displayOrder=""
    articleId="WindowsBootManager-0xC000014C-STATUS_REGISTRY_CORRUPT"
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
We have investigated and determined that your virtual machine (VM) <!--$vmname-->**[vmname]**<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code **0xC000014C**. This issue occurs when one of the files that contains registry data is corrupt, the image of the file in memory is corrupt, or the file could not be recovered because the alternate copy or log was absent or corrupt.  You can use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.VirtualMachineSerialConsoleLogBlade) to see the current state of your VM.  For this issue, the screenshot would reflect the error code **0xC000014C**.<br>
<!--/issueDescription-->

## **Recommended Steps**
To fix the VM, please follow the troubleshooting steps indicated below:

1. Please make a note of the file name and the path from the screenshot from the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->
2. If the file name refers to the file *\Windows\system32\config\SYSTEM* then save a copy of the OS disk.  (See [Create a copy of a specialized Windows VM running in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-vhd-copy))
3. Attach the copy/snapshot of the OS disk of the VM as a data disk to another VM (a troubleshooting VM). For more information, see [How to attach a data disk to a Windows VM in the Azure portal](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-attach-disk-portal).
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned.
5. Mount the SYSTEM hive of your VM.

  * Open **Regedit.exe**.
  * Click on **HKEY_LOCAL_MACHINE** and from the **File** menu select **Load Hive...**.
  * Browse to the the file **<drive letter>:\Windows\system32\config\SYSTEM**, where **drive letter** is from the attached disk.
  * When prompted for a name, use **BROKENSYSTEM**.
6. Determine state of the SYSTEM hive.
    
    a. If the hive fails to open with the following error, open a support case.
    ```
    Cannot Load C:\<path to hive>\SYSTEM: Error while loading the hive.
    ```
    b. If the hive opens up with no issues then the hive may not have been closed properly.  Proceed with the next step.
7. Unload the SYSTEM hive
8. At this time you may want to enable Azure Serial Console, this will allow for quicker resolutions to issues in the future.  First identify the Boot partition and the Windows partition. If there is only one partition on the OS disk, this partition is the both the Boot partition and the Windows partition.

    * The Windows partition contains a folder named "Windows," and this partition is larger than the others.
    * The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB
9. Run the following command line as an administrator, and then record the identifier of Windows Boot Loader (not Windows Boot Manager). The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step

      ```
      bcdedit /store [Boot partition]:\boot\bcd /enum
      ```
10. If you want to enable Azure Serial Console on this machine, then please also run these following extra flags:

    ```
    bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} displaybootmenu yes
    bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} timeout 5
    bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} bootems yes
    bcdedit /store [Boot partition]:\boot\bcd /ems {[Identifier]} ON
    bcdedit /store [Boot partition]:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
    ```
11. Detach the repaired OS disk from the troubleshooting VM. [Then, swap the OS disk from the original VM](https://docs.microsoft.com/azure/virtual-machines/windows/os-disk-swap)
