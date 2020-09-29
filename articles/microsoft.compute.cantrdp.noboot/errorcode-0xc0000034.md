<properties
pageTitle="VM boot error"
description="Virtual machine failed to boot with error code 0xc0000034"
infoBubbleText="A boot error has been found. See details on the right."
service="microsoft.compute"
resource="virtualmachines"
authors="ram-kakani, timbasham, jasonbandrew"
ms.author="ramakk, tibasham, v-jasoan"
displayOrder=""
articleId="VMCannotRDP_E32BD6A1-9532-4AC6-835D-4ECB4A074CE5"
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
We have have investigated and identified that your VM <!--$vmname-->[vmname]<!--/$vmname--> is currently in an inaccessible state because windows failed to boot with error code **0xc0000034**. This occurs when there is an issue with the boot configuration data and the booting partition is unable to find the windows folder.<br>

If you find that you cannot connect to a VM in the future, you can view a screenshot of your VM using the boot diagnostics blade in the Azure Portal. This may help you diagnose the issue and determine if a similar boot error is the cause.<br>
<!--/issueDescription-->

## **Recommended Steps**
To fix the BCD store, follow the troubleshooting steps indicated below:

1. Delete the virtual machine <!--$vmname-->[vmname]<!--/$vmname-->. Make sure that you select the keep the disks option when you do this.
2. [Save a copy of the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/vhd-copy)
3. [Attach the OS disk of the deleted VM as a data disk to another VM (a troubleshooting VM)](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal)
4. Connect to the troubleshooting VM to ensure the newly attached OS disk is online and has a drive letter assigned
5. Identify the Boot partition and the Windows partition. If there's only one partition on the OS disk, this partition is both the Boot partition and the Windows partition. The Windows partition contains a folder named "Windows," and this partition is larger than the others. The Boot partition contains a folder named "Boot." This folder is hidden by default. To see the folder, you must display the hidden files and folders and disable the Hide protected operating system files (Recommended) option. The boot partition is typically 300 MB~500 MB.
6. Run `bcdedit /store [Boot partition]:\boot\bcd /enum` as an administrator, and record the identifier of Windows Boot Loader (not Windows Boot Manager). You will find the reference to the partition {bootmgr} is missing on the boot database. The identifier is a 32-character code and it looks like this: xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.  You will use this identifier in the next step
7. Repair the Boot Configuration data by running the following command lines. You must replace these placeholders by the actual values. "Windows partition" is the partition that contains a folder named "Windows", "Boot partition" is the partition that contains a hidden system folder named "Boot", and "Identifier" is the identifier of Windows Boot Loader you found in the previous step:

```
bcdedit /store [BCD FOLDER - DRIVE LETTER]:\boot\bcd /create {bootmgr}
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} description "Windows Boot Manager"
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} locale en-us
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} inherit {globalsettings}
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} displayorder [IDENTIFIER FROM THE STEP BEFORE THIS ONE]
bcdedit /store [Boot partition]:\boot\bcd /set {bootmgr} timeout 30
```

8. Ensure the boot setup is setup properly by executing the command in step 6: `bcdedit /store [Boot partition]:\boot\bcd /enum`
9. Detach the repaired OS disk from the troubleshooting VM. [Then, create a new VM from the OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized).
