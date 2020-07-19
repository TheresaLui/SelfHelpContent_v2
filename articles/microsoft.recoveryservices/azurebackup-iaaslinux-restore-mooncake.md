<properties
	pageTitle="Azure Linux VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="23"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-iaaslinux-restore-mooncake"
	ownershipId="Compute_SiteRecovery"
/>

# Azure Linux VM Restore Limitations

## **Recommended Steps**

**Known Limitations**

- Restoring backed-up VMs across Zone/Region/subscription or V-Net is not supported. For more information, see [supported scenarios](https://docs.azure.cn/backup/backup-support-matrix-iaas#support-for-vm-management) for VM management.
- Files/Folders restore limitation on having special configuration [**Dynamic Disks or LVM/RAID Arrays**](https://docs.azure.cn/backup/backup-azure-restore-files-from-vm#special-configurations)
- Restore disks will restore all disks (OS and data disks attached to the VM). Individual disk restore is not available using this option.
- Replacing an existing virtual machine during restore is not supported. You can use one of the following restore options:

	- [Replace disks of existing backed-up VM](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#replace-existing-disks)
	- [Restore disks](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-disks) and create a new VM using [Templates](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm) or [PowerShell](https://docs.azure.cn/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)
	- [Restore as a new VM](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#create-a-vm)
	
**Frequently Asked Questions**

- [Restore specific files or folders from Azure Virtual Machine backup](https://docs.azure.cn/backup/backup-azure-restore-files-from-vm)
- Restore to latest or specific recovery point using [Portal](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#select-a-restore-point) or [PowerShell](https://docs.azure.cn/backup/backup-azure-vms-automation#restore-an-azure-vm)
- [Configure static IP address to restored VM](https://docs.azure.cn/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)
- [Restore an Encrypted VM](https://docs.azure.cn/backup/backup-azure-vms-encryption)
- [Restore when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault](https://docs.azure.cn/backup/backup-azure-restore-key-secret)
- [Restore a Domain Controller VM](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)
- [Restore VM with special configurations](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)
- Attach an existing NIC to the restored VM:
	
	- Step 1: [Remove from original VM](https://docs.azure.cn/virtual-network/virtual-network-network-interface-vm#remove-a-network-interface-from-a-vm)
	- Step 2: [Attach to restored VM](https://docs.azure.cn/virtual-network/virtual-network-network-interface-vm#vm-add-nic)

- If you are unable to restore, verify that you don’t have any group policy restriction from portal
- We recommend using SSH based authentication for Linux VMs. If you are using password based authentication on the backed up VM, you need to [reset password](https://docs.microsoft.com/previous-versions/azure/virtual-machines/linux/classic/reset-access-classic) post restore using VM Access extension
- If you are unable to see **Backup Items** from the portal, ensure you have [required permission](https://docs.azure.cn/backup/backup-rbac-rs-vault) to access backup vault
- If you are facing issues restoring a VM, try [Restore disks](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-disks) and create a new VM using [Templates](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm) or [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)
- To perform a restore ensure you have appropriate [Role Based Access Controls in place](https://docs.azure.cn/backup/backup-rbac-rs-vault)
- To restore a VM into a specific availability set, [Restore disks](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-disks) and create a VM in availability sets using PowerShell cmdlets
- In case of Azure datacenter disaster, Azure Backup [restores VM in paired datacenter](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)

## **Recommended Documents**

- [Azure Virtual Machine restore troubleshooting guide](https://docs.azure.cn/backup/backup-azure-vms-troubleshoot#restore)
- [Restore Azure Virtual Machine using portal](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#choose-a-vm-restore-configuration)
- [Restore Azure Virtual Machine using PowerShell](https://docs.azure.cn/backup/backup-azure-vms-automation#restore-an-azure-vm)
