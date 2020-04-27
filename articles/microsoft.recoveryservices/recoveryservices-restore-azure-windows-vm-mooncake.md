
<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
	articleId="e723877c-83f3-49fa-81f1-24ad6ec643a1"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure VM Restore Limitations

## **Limitations when restoring a VM**
Following limitations apply when restoring a Azure VM from backup. 

* Replacing an existing virtual machine during restore is not supported. Please create a new virtual machine from backup or restore disks from backup and use disks and configuration to create a new VM.

* Cross region and cross-subscription restore is not supported i.e. if your VM which got backed up is in China North, you can only restore to China North in same subscription. 

* For Domain Controller VMs, we recommend using Restore Disks and creating a new VM from restored disks. 

* To Restore a VM into a specific availability set, restore disks and configuration, and create a VM using PowerShell cmdlets. [Learn More](https://docs.azure.cn/backup/backup-azure-vms-automation#restore-an-azure-vm)

* If you are facing issues restoring a virtual machine, please try restore disks and use restored disks to create a virtual machine. 

* Restore disks will restore all disks(OS and data disks attached to the VM). Individual disk restore is not possible using this option. 

* In case of Azure Datacenter Disaster, Azure Backup restores VM in paired data center. [Learn More](https://docs.azure.cn/backup/backup-azure-restore-vms#restoring-a-vm-during-azure-datacenter-disaster)


## **Recommended documents**
[Azure virtual machine restore troubleshooting guide](https://docs.azure.cn/backup/backup-azure-vms-troubleshoot)<br>
[How to restore virtual machine using portal](https://docs.azure.cn/backup/backup-azure-arm-restore-vms)<br>
[How to restore virtual machine using PowerShell](https://docs.azure.cn/backup/backup-azure-vms-automation#restore-an-azure-vm)<br>
