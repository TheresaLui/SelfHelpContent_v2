<properties
    pageTitle="VM boot error: Operating system not found"
    description="Virtual machine failed to boot because an operating system wasn't found."
    infoBubbleText="A boot error occurred your VM during with the message 'An operating system wasn't found'."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="BootError-OS_NOT_FOUND"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Operating system not found

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because either the OS boot process couldn't locate an active system partion, or there is BCD corruption which resulted in a missing reference to the Windows partition on the BCD store. Alternatively, it could also be due to a ransomware attack.
<!--/issueDescription-->

When you use [Boot diagnostics](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics) to view the screenshot of the VM, you will see that the screenshot displays the message: `An operating system wasn't found. Try disconnecting any drivers that don't contain an operating system. Press Ctrl+Alt+Del to restart`.<br>

## **Recommended Steps**

1. First, use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to prepare a Repair VM and then connect to it using Remote Desktop Connection
2. After preparing the repair VM, follow the directions in either **Generation 1** or **Generation 2** VMs section
3. If you are still unable to resolve the issue using the previous steps, then go to the **directions for a ransomware attack** section

### Directions for a Generation 1 VM

1. Open an elevated command prompt (run as administrator) and enter `bcdedit /store <Letter of the boot partition>:\boot\bcd /enum` to list the BCD store data. Replace `<Letter of...>` within the command with the value indicated. The path should be `\windows\system32\winload.exe`.
2. Once listed, note the Windows Boot Loader **identifier** value, which you will use later. If this errors out because there's no `\boot\bcd` file, then skip ahead to the **directions for a ransomware attack** section.
3. In the elevated command prompt, enter `diskpart` to open the DISKPART tool
4. List, then select the added disk using the commands below. Replace `<# of disk>` with the added disk number:

```
list disk
sel disk <# of disk>
```

5. List, then select the *System Managed* partition using the commands below. Replace `<# of partition>` with the partition number. This partition is typically about 350MB in size:

```
list partition
sel partition <# of partition>
```

6. Check the status of the partition by entering the `detail partition` command:

	1. If `Active: No` is displayed, then enter the command `active` to change the *Active* flag. You can run `detail partition` again to verify it was done properly.
	2. Once set to active, enter `exit` to close the DISKPART tool
	3. Now test if this has fixed your VM. If unsuccessful, continue to the next step.

7. Enter the following commands. Replace `<text here>` with the information specified:

```
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} device partition=<BCD FOLDER - DRIVE LETTER>:
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} device partition=<WINDOWS FOLDER - DRIVE LETTER>:
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} osdevice partition=<WINDOWS FOLDER - DRIVE LETTER>:
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```

* If the VHD has a single partition and both the BCD Folder and Windows Folder are in the same volume, then the setup above might not work. If that is the case, try replacing the partition values with `boot`:

```
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} device boot
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} device boot
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} osdevice boot
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```

8. [Use step 5 of the VM repair commands to reassemble the VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example)

	1. Test if this has fixed your VM. If unsuccessful, continue to the next step.

9. Use [step 3 of the VM Repair commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to attach the disk to your Repair VM

10. Backup the `\boot` folder, then run the following commands:

	* Create a copy of the built-in BCD template that comes within each Windows installation: `bcdboot <WINDOWS FOLDER - DRIVE LETTER>:\windows /s <BCD FOLDER - DRIVE LETTER>: /v /f BIOS`
	* Add the following flags, which are not there by default:

```
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER FROM THE BOOT LOADER>} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER FROM THE BOOT LOADER>} recoveryenabled Off
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER FROM THE BOOT LOADER>} bootstatuspolicy IgnoreAllFailures
```

* Enable EMS to enable the serial console feature:

```
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} displaybootmenu yes
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} timeout 5
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} bootems yes
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /ems {current} on
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
```

10. [Use step 5 of the VM repair commands to reassemble the VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) and then test if this has fixed your VM. If unsuccessful, continue to the **ransomware attack directions** section.

### Directions for a Generation 2 VM

1. In Windows search, type `Disk Management` and then open the **Disk Management** tool

	* Identify the disk number of the disk that was attached to your repair VM (typically the most recent/highest numerical value)
	* Within that disk, identify the partition containing `EFI System Partion` that has no assigned letter. This partition holds the BCD store you will modify later.

2. Open an elevated command prompt (run as administrator) and enter `diskpart` to launch the diskpart tool
3. List the disks on the system and then select the attached disk identified earlier. Replace `<# of attached disk>` with the number of the disk:

```
list disk
sel disk <# of attached disk>
```	

4. List the partitions and then select the EFI partition that was identified earlier. Replace `<# of partition>` with the partition number. This partition is typically about 100MB.

```
list partition
sel partition <# of partition>
```
	
5. Now that the partition is selected, enter `assign` to assign a letter to the partition. You can verify your steps using the Disk Managment tool to see if the partition now has an assigned letter.
6. Enter `bcdedit /store <Letter you assigned to the EFI System partition>:EFI\Microsoft\boot\bcd /enum` to list the BCD store data. Replace `<Letter of...>` within the command with the value indicated. The path should be `\windows\system32\winload.efi`.

	1. Once listed, note the Windows Boot Loader **identifier** value, which you will use later
	2. If this errors out because there's no `\boot\bcd` file, then skip ahead to the **ransomware attack directions** section

7. Enter the following commands:

```
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {bootmgr} device partition=<Volume Letter of EFI System Partition>:
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {bootmgr} integrityservices enable
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} device partition=<WINDOWS FOLDER - DRIVE LETTER>:
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} integrityservices enable
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} osdevice partition=<WINDOWS FOLDER - DRIVE LETTER>:
bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```

8. [Use step 5 of the VM Repair commands to reassemble the VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example). Test if this has fixed your VM. If unsuccessful, continue to the next step.
9. Use [step 3 of the VM Repair commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to attach the disk to your Repair VM
10. Backup the `\boot` folder, then run the following commands:

	* Create a copy of the built-in BCD template that comes within each Windows installation using `bcdboot <WINDOWS FOLDER - DRIVE LETTER>:\windows /s <Volume Letter of EFI System Partition>: /v /f UEFI`
	* Add the following flags, which are not there by default: 

```
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} integrityservices enable
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures
```	    

* Enable EMS to enable the serial console feature:

```	
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} displaybootmenu yes
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} timeout 5
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} bootems yes
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /ems {current} on 
bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /emssettings EMSPORT:1 EMSBAUDRATE:115200
```

11. [Use step 5 of the VM repair commands to reassemble the VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) and then test if this has fixed your VM. If unsuccessful, continue to the **ransomware attack directions** section.

### Directions for a Ransomware Attack

1. Open a **File Explorer** window and navigate to **View > Options > Change folder and search options**
1. In the pop-up window, click the **View** tab, select the **Show hidden files, folders, and drives** radio, then click **Apply**. Then close the pop-up window.
1. Open your disk and see if there's any ".txt" file in the root folder with instructions on how to regain access to the files of the VM
1. If you encounter any files of this nature, then the [VM needs to be restored from backup or rebuilt](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)
1. If there are security concerns, you can [open a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade)

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
