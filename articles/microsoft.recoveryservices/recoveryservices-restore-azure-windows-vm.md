<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Azure Windows VM Restore Limitations

## **Recommended Steps**
**Limitations**<br>
* **Replacing an existing virtual machine during restore is not supported**. Please create a new virtual machine from backup or restore disks from backup and use disks and configuration to create a new VM. Using [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms), Using [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm), from [restored disk](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks) <br>
* If you are facing issues restoring a virtual machine, please try *Restore Disk* functionality: 
  * **Step 1** - [*Restore Disks*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#choose-a-vm-restore-configuration) functionality. 
  * **Step 2** - Use the disk that was restored to [*create a virtual machine*](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks).<br>
* **Cross region and cross-subscription restore is not supported** i.e. if your VM which got backed up is in West Europe, you can only restore to West Europe in same subscription.<br>
* [File/Folder restore limitation with special configuration - **Dynamic Disks, Storage Spaces**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#special-configurations) <br>
* If you are **unable to restore**, verify that you don’t have any group policy restriction in place from portal.<br>
* If you are **unable to see backup items** from the portal then ensure you have [required permission](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) to access backup vault. <br>
* [Ensure you have appropriate Role Based Access controls in place.](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) <br>

**Frequently Asked Questions:**<br>
* [*How can I restore specific files or folders from IaaS VM?*](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)<br>
* *How to restore IaaS VM to latest/specific recovery point?* Using [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms), Using [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm), from [restored disk](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks), when Key (Key Encryption Key) and Secret (BitLocker Encryption Key) [does not exist in the key vault.](https://docs.microsoft.com/azure/backup/backup-azure-restore-key-secret)<br>
* [*How to configure static IP address to restored VM?*](https://docs.microsoft.com/azure/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)<br>
* [*How to restore an Encrypted VM?*](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption)<br>
* [*How to restore a Domain Controller VM?*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-domain-controller-vms) For Domain Controller VMs, we recommend using Restore Disks and creating a new VM from restored disks.<br>
* [*How much will it take to restore VM?* Understand factors contributing to restore time.](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#total-restore-time)<br>
* *How can I attach existing NIC to the restored VM?* Follow [steps](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-remove-nic) to remove from original VM and [steps](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-add-nic) to attach to restored VM.<br>
* [*How to restore VM with special network configurations?*](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-vms-with-special-network-configurations)<br>

## **Recommended documents**
[Azure virtual machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#backup-or-restore-taking-time)<br>
[How to restore virtual machine using portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)<br>
[How to restore virtual machine using PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)<br>
