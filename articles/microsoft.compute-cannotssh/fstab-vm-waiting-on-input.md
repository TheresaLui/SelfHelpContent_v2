<properties
	pageTitle="VM boot error"
	description="Linux VM waiting on input"
	infoBubbleText="Found a file system table related issue. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="craigwiand"
	displayOrder="1"
	articleId="VMCannotSSH_D798E6ED-7353-480D-8825-51C2729DD5BA"
	diagnosticScenario="CantSSH"
	selfHelpType="diagnostics"
	supportTopicIds="32411835"
	resourceTags="linux"
	productPesIds="15571"
	cloudEnvironments="public"
/>

# Diagnostics on your Linux Virtual machine found a boot error
<!--issueDescription-->
## **Boot error found for your virtual machine <!--$vmname-->[vmname]<!--/$vmname-->:**
Microsoft Azure has concluded an investigation of your  virtual machine. We identified that your VM is currently in an inaccessible state because it is waiting on user input to continue the boot process. This problem is most commonly due to a problem in the file system table(fstab) file.

You can use the Azure Portal to view the [serial log](data-blade:Microsoft_Azure_Classic_Compute.VirtualMachineSerialConsoleLogBlade) output of your VM in the boot diagnostics blade to detect connectivity issues due to similar boot failures in the future.

More information on the fstab errors can be found in the article [Azure Linux VM cannot start because of fstab error](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors)
<!--/issueDescription-->

## **Recommended Steps**
To recover the virtual machine, follow these steps:

1. Access [serial console](data-blade:Microsoft_Azure_Compute.SerialConsoleBlade) of your VM <!--$vmname-->[vmname]<!--/$vmname-->

2. If the VM is configured, press M for manual recovery to enter single user mode or login as root.  If the VM is not configured, reboot the VM using the Azure portal while holding down the ESC key.  If you are presented with a grub prompt enter ‘c’ for command prompt.

	a. Change into /etc directory and backup your fstab file.
	```
	cd /etc/
	cp fstab fstab_orig
	```
	b. View and verify the contents of the fstab file `cat /etc/fstab`

	c. Run `blkid` and compare the names and UUIDs of the partitions on this VM with the entries in your fstab file.

	d. Edit the fstab file to remove or comment out using a # any incorrect entries using your favorite text editor, for example:
`nano /etc/fstab` or `vi /etc/fstab`

	e. Validate that updates and test the syntax before initiating a reboot `$ sudo mount -a`

	f. Reboot the VM and test SSH access.

3. In case serial console cannot be accessed, please follow the steps at article [Azure Linux VM cannot start because of fstab errors](https://support.microsoft.com/help/3206699) to resolve the issue.

## **Recommended documents**
[How to use boot diagnostics to troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)<br>
[Azure Virtual Machine Serial Console](http://aka.ms/serialconsolehelp)
