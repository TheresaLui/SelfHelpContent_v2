<properties
    pageTitle="VM boot error: Loading Windows Files"
    description="Virtual machine failed to boot due to the Windows Boot Manager menu"
    infoBubbleText="A Windows Boot Manager prompt 'Choose an operating system to start, or press TAB to select a tool:'"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="mibufo"
    ms.author="v-mibufo"
    displayOrder=""
    articleId="OSStartUp-LOADING_WINDOWS_FILES"
    diagnosticScenario="booterror"
    selfHelpType="diagnostics"
    supportTopicIds="32411835"
    resourceTags="windows"
    productPesIds="14749"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# VM boot error: Loading Windows Files
<!--issueDescription-->
We have investigated and determined that your virtual machine (VM) <!--$vmname-->[vmname]<!--/$vmname--> is in an inaccessible state because the OS was set to start in a mode other than 'Normal'. If set to Diagnostic Startup, Selecting Startup, Safe boot minimal, Safe boot AlternativeShell, or Safe boot Network, the OS will load Windows in a debug/diagnostic mode.
<!--/issueDescription-->

Use the [Boot Diagnostics Screenshot](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) to see the current state of your VM. For this issue, the screenshot would show the **Loading Windows** screen which lists the system files as they are loaded. This may also help you diagnose future issues and determine if a boot error is the cause.<br>

## **Recommended Steps**

1. Use [steps 1-3 of the VM Repair Commands](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/repair-windows-vm-using-azure-virtual-machine-repair-commands) to prepare a Repair VM and then use Remote Desktop Connection connect to it.

2. If you are using a Generation 2 VM, you will need to first do the following to assign a letter to the EFI partition:

	1. In Windows search, enter `disk management` and then select the Disk Management app.

	2. Identify the attached broken disk. Usually it's the most recently added disk with the name that's the highest numerical value.

	3. Identify the partition in that disk that is labeled `EFI System Partition` that holds the BCD store.

		> These partitions are typically smaller and are around 100MB in size.

	4. Open an elevated command prompt (run as administrator) and enter `diskpart` to launch the DISKPART tool.

	5. Enter `list disk` and then enter `sel disk <DISK NUMBER>` to select the attached broken disk.

		> Replace `<DISK NUMBER>` with the number of the disk you identified in sub-step 2.

	6. Enter `list part` and then enter `sel part <PARTITION NUMBER>` to select the unassigned partition.

		> Replace `<PARTITION NUMBER>` with the number of the unassigned partition you identified in sub-step 3.

	7. Enter `assign` to assign a letter to the selected partition.

3. In Windows search, enter `disk management` and then select the Disk Management app.

	1. Identify the attached broken disk. Usually it's the most recently added disk with the name that's the highest numerical value.

	2. If the disk is set to **OFFLINE**, then right-click on it and set it to **ONLINE**.

	3. If the disk is encrypted, then follow the [directions to decrypt the encrypted disk](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-bitlocker-boot-error) before proceeding.

4. If the disk has multiple partitions, identify the partition that has `\boot\bcd`.

	> This partition is often listed as **System Reserved** and in a Generation 2 VM is the partition that was left unassigned prior to step 2.

	1. Right-click on the partition you wish to investigate and select **Open**.

	2. In the File Explorer window that opens, navigate to **View > Options > Change folder and search options**.

	3. In the pop-up window, select the **View** tab, select the **Show hidden files, folders, or drives** radio, and also uncheck **Hide protected operating system files (Recommended)**.

	4. Check for a `boot` folder with the `BCD` file inside it, or type `\boot\bcd` in File Explorer search.

	5. Note the partition identified here. If you don't find `\boot\bcd` in this partition, continue checking the other partitions until you locate it.

5. Open an elevated command prompt (run as administrator) and enter `bcdedit /store <DISK LETTER>:\boot\bcd /enum`.

	> Replace `<DISK LETTER>` with the letter of the attached broken disk.

	1. Note the identifier of the Windows Boot Loader/Partition of the `\Windows` partition. It is standard for the identifier value to be set to the value of `<default>`.

	2. Check if the `safeboot` flag is also listed under the Windows Boot Loader/Partition.

6. If *safeboot* was listed, then enter `bcdedit /store <DISK LETTER>:\boot\bcd /deletevalue {<IDENTIFIER>} safeboot ` to delete the flag.

	> Replace `<DISK LETTER>` with the letter of the attached broken disk.

	> Replace `<IDENTIFIER>` with the identifier from step 5.

	3. Enter `bcdedit /store <PARTITION LETTER>:\boot\bcd /enum` again to verify *safeboot* was removed.

		> Replace `<PARTITION LETTER>` with the letter of the `\boot\bcd` partition.

## **Recommended Documents**

* [Troubleshoot RDP Issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/rdp)
