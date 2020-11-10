<properties
	pageTitle="VM boot error"
	description="Incorrect UUID in fstab"
	infoBubbleText="We found a file system table related issue. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="craigwiand,timbasham"
	ms.author="tibasham"
	displayOrder="1"
	articleId="VMCannotSSH_72059703-AD61-42AF-BF8A-991A7DEFA197"
	diagnosticScenario="CantSSH"
	selfHelpType="diagnostics"
	supportTopicIds="32411835"
	resourceTags="linux"
	productPesIds="15571,15797,16454,16470"
	cloudEnvironments="public,mooncake, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# Diagnostics on your Linux Virtual machine found a boot error
<!--issueDescription-->
Microsoft Azure has concluded an investigation of your virtual machine. We identified that your VM is currently in an inaccessible state because the file system table (fstab) file contains an entry using a universally unique identifier (UUID) for a file system that is not present on the VM. This condition can have several causes, including removing a data disk and restarting without updating the fstab file.
<!--/issueDescription-->


## **Recommended Steps**

1. Access the [serial console](data-blade:Microsoft_Azure_Compute.VmSerialConsoleValidationBlade.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/serialConsole) of your VM <!--$vmname-->[vmname]<!--/$vmname-->
2. If the VM is configured, press M for manual recovery to enter single user mode or login as root. If the VM is not configured, reboot the VM using the Azure portal while holding down the ESC key. If you are presented with a grub prompt, enter ‘c’ for command prompt.

	* Change into /etc directory and backup your fstab file:

	```
	cd /etc/
	cp fstab fstab_orig
	```

	* View and verify the contents of the fstab file `cat /etc/fstab`
	* Run `blkid` and compare the names and UUIDs of the partitions on this VM with the entries in your fstab file
	* Edit the `fstab` file to remove or comment out (with `#` symbol) any incorrect entries using your favorite text editor, for example: `nano /etc/fstab` or `vi /etc/fstab`
	* Before initiating a reboot, validate changes to `fstab` and check the syntax is correct by running `$ sudo mount -a`
	* Reboot the VM and test SSH access

3. In case serial console cannot be accessed, please follow the steps in the article [Azure Linux VM cannot start because of fstab errors](https://support.microsoft.com/help/3206699) to resolve the issue

## **Recommended Documents**

* [How to use boot diagnostics to troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)<br>
* [Azure Virtual Machine Serial Console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-linux)
* Use the Azure Portal to view the [serial log](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) output of your VM in the boot diagnostics blade to detect connectivity issues due to similar boot failures in the future
