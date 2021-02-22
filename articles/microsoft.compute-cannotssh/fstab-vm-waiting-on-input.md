<properties
	pageTitle="VM boot error"
	description="Linux VM waiting on input"
	infoBubbleText="Found a file system table related issue. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="craigwiand,timbasham"
	ms.author="tibasham"
	displayOrder="1"
	articleId="VMCannotSSH_D798E6ED-7353-480D-8825-51C2729DD5BA"
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
Microsoft Azure has concluded an investigation of your  virtual machine. We identified that your VM is currently in an inaccessible state because it is waiting on user input to continue the boot process. This problem is most commonly due to a problem in the file system table(fstab) file.
<!--/issueDescription-->

## **Recommended Steps**

* To restore access to the VM, follow the steps in the [Linux VM starting issues due to fstab errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/linux-virtual-machine-cannot-start-fstab-errors) troubleshooting guide

## **Recommended Documents**

* [How to use boot diagnostics to troubleshoot Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)<br>
* [Azure Virtual Machine Serial Console](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-linux)
* Use the Azure Portal to view the [serial log](data-blade:Microsoft_Azure_Compute.SerialConsoleLogBladeViewModel.resourceId.$resourceId;data-blade-uri:{$domain}/#@microsoft.onmicrosoft.com/resource/{$resourceIdDecoded}/bootDiagnostics) output of your VM in the boot diagnostics blade to detect connectivity issues due to similar boot failures in the future
* [Azure Linux VM cannot start because of fstab error](https://support.microsoft.com/help/3206699/azure-linux-vm-cannot-start-because-of-fstab-errors)
