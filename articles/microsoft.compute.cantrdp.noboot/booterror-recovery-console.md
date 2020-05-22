<properties
    pageTitle="VM boot error: Recovery Console"
    description="Virtual machine failed to boot and displays the recovery console, which depending upon the OS version you are running will prompt the you to begin a process labeled: recovery, startup repair, automatic repair, etc."
    infoBubbleText="A boot error occurred your VM which launched the recovery console."
    service="microsoft.compute"
    resource="virtualmachines"
    authors="michaeljbuford"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="BootError-RECOVERY_CONSOLE"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM Boot Error: Recovery Console

<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because Windows failed to boot with error code **Recovery**, **System Recovery Options**, **Startup Repair**, **Automatic Repair**, **Choose an option** or **Choose your keyboard layout**. If you encounter this error message, it means that either there isn’t enough space on the C: drive, or the image was uploaded from on-premises and doesn't have the Binary Coded Decimal (BCD) store setup properly.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would reflect the error code **Recovery**, **System Recovery Options**, **Startup Repair**, **Automatic Repair**, **Choose an option** or **Choose your keyboard layout**. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands) to prepare a Repair VM and then use Remote Desktop Connection connect to it.

2. To make sure there's enough space on the C: drive, [expand it to 1 Tb](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk) and then perform disk cleanup:

	1. First, [detach the data disk from broken VM](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell).

	2. Next, [attach the data disk to a functioning VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm).

	3. Now use the [Disk Cleanup tool](https://support.microsoft.com/help/4026616/windows-10-disk-cleanup) to free up space.

	4. Optionally, do a defragmentation on the drive using the following command: `defrag <LETTER ASSIGNED TO THE OS DISK>: /u /x /g`

		> Replace `<LETTER ASSIGNED TO THE OS DISK>` in the command with the appropriate letter of your drive.

3. Determine the Windows Boot Loader identifier: 

	1. Open an elevated CMD instance and enter `chkdsk <DRIVE LETTER>: /f` to run CheckDisk.

		> Replace `<DRIVE LETTER>` in the command with the appropriate letter of your drive.

	2. Gather the boot setup info using one of the following commands:

			Generation 1 VM:
			bcdedit /store <DRIVE LETTER>:\boot\bcd /enum

			Generation 2 VM:
			bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /enum

		> If you encounter an error because there's no BCD file, then [open a support ticket](https://azure.microsoft.com/support/create-ticket/) and disregard the rest of this article.

	3. Note the boot identifier displayed. The path for a Generation 1 VM will be `\windows\system32\winload.exe` whereas for a Generation 2 VM the path will be `\windows\system32\winload.efi`.

4. Using the identifier, enter the commands below for your VM type. Make sure to replace any `<TEXT>` with the information specified.

		Generation 1 VM:
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} device partition=<BCD FOLDER - DRIVE LETTER>
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} integrityservices enable
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} device partition=<WINDOWS FOLDER - DRIVE LETTER>
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} integrityservices enable
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} osdevice partition=<WINDOWS FOLDER - DRIVE LETTER>
		bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures

		Generation 2 VM:
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {bootmgr} device partition=<Volume Letter of EFI System Partition>:
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {bootmgr} integrityservices enable
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} device partition=<WINDOWS FOLDER - DRIVE LETTER>:
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} integrityservices enable
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} osdevice partition=<WINDOWS FOLDER - DRIVE LETTER>:
		bcdedit /store <Volume Letter of EFI System Partition>:EFI\Microsoft\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures

	1. If you are using a Generation 1 VM, the setup above didn’t work, the VHD has a single partition, and both the BCD Folder and Windows Folder are in the same volume, then try replacing the partition values with `boot`:

			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} device boot
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {bootmgr} integrityservices enable
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} device boot
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} integrityservices enable
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} recoveryenabled Off
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} osdevice boot
			bcdedit /store <BCD FOLDER - DRIVE LETTER>:\boot\bcd /set {<IDENTIFIER>} bootstatuspolicy IgnoreAllFailures

5. [Detach the disk](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk) and wait till Azure updates the disk lease (3 minutes or less), then [use step 5 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands#repair-process-example) to reassemble the VM.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
