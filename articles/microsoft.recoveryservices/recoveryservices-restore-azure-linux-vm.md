<properties
	pageTitle="Azure VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32553297"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Azure VM Restore Limitations
Following limitations apply when restoring a Linux Azure VM from backup. 

* Replacing an existing virtual machine during restore is not supported. Please create a new virtual machine from backup or restore disks from backup and use disks and configuration to create a new VM.

* Cross region and cross-subscription restore is not supported i.e. if your VM which got backed up is in West Europe, you can only restore to West Europe in same subscription. 

* For Domain Controller VMs, we recommend using Restore Disks and creating a new VM from restored disks. 

* We recommend using SSH based authentication for Linux VMs. If You are using Password based authentication on the VM which got backed up, you need to [reset password](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-classic-reset-access/) post restre using VM Access extension. 

* To Restore a VM into a specific availability set, restore disks and configuration, and create a VM using PowerShell cmdlets. [Learn More](https://azure.microsoft.com/documentation/articles/backup-azure-vms-automation/#restore-an-azure-vm)

* If you are facing issues restoring a virtual machine, please try restore disks and use restored disks to create a virtual machine. 

* In case of Azure Datacenter Disaster, Azure Backup restores VM in paired data center. [Learn More] (https://azure.microsoft.com/documentation/articles/backup-azure-restore-vms/#restoring-a-vm-during-azure-datacenter-disaster)

## **Recommended documents**
[Azure virtual machine restore troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>
