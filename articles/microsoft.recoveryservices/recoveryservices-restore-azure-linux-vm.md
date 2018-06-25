<properties
	pageTitle="Azure Linux VM Restore Limitations"
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

# Azure Linux VM Restore Limitations

## **Recommended Steps**
**Limitations**<br>
* **Replacing an existing virtual machine during restore is not supported**. Please create a new virtual machine from backup or restore disks from backup and use disks and configuration to create a new VM. Using [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms), Using [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm), from [restored disk](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks) <br>
* If you are facing issues restoring a virtual machine, please try *Restore Disk* functionality: 
  * **Step 1** - [*Restore Disks*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#choose-a-vm-restore-configuration) functionality. 
  * **Step 2** - Use the disk that was restored to [*create a virtual machine*](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks).<br>
* **Cross region and cross-subscription restore is not supported** i.e. if your VM which got backed up is in West Europe, you can only restore to West Europe in same subscription.<br>
* If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal.<br>
* If you are **unable to see backup items** from the portal then ensure you have [required permission](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) to access backup vault. <br>
* [Ensure you have appropriate Role Based Access controls in place](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) 
* We recommend using SSH based authentication for Linux VMs. If You are using Password based authentication on the VM which got backed up, you need to [reset password](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-classic-reset-access/) post restre using VM Access extension. <br>
* To Restore a VM into a specific availability set, restore disks and configuration, and create a VM use PowerShell cmdlets. [Learn More](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm) <br>
* In case of Azure Datacenter Disaster, Azure Backup [restores VM in paired data center](https://docs.microsoft.com/azure/backup/backup-azure-restore-vms#restoring-a-vm-during-azure-datacenter-disaster) <br>
* Restore disks will restore all disks(OS and data disks attached to the VM). Individual disk restore is not possible using this option. <br>
* [Azure virtual machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot/)<br>
