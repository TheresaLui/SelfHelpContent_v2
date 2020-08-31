<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	ms.author="trinadhk"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6fff7f67-d153-43f0-89c9-598eba2fe465"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Windows VM Restore Limitations

## **Recommended Steps**

<properties
	pageTitle="Azure Windows VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	ms.author="trinadhk"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6fff7f67-d153-43f0-89c9-598eba2fe465"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Windows VM Restore Limitations

## **Recommended Steps**

- [Options to restore (un)managed or (un)encrypted VM](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)
- [How do Restore disks](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks) and create a new VM using [ARM templates](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm), [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks) or [Azure CLI](https://docs.microsoft.com/azure/backup/tutorial-restore-disk)
- [Permissions/RBAC roles](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#before-you-start) required before performing a restore
- How to restore: [selective disk](https://docs.microsoft.com/azure/backup/selective-disk-backup-restore#selective-disk-restore), [encrypted Azure VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm), [selective files and folders](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-the-volume-and-copy-files)?
- [Recovering files from an Encrypted Azure VM is currently not supported](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-file-level-restore). Alternatively, you can [restore disk of the encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm) and copy the required files
- Special restore configuration requirements for [Dynamic disks, Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#special-configurations)
- [Guidelines for restoring VM with large disk size(>4TB) and disk count(>16 disks)](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#file-recovery-from-virtual-machine-backups-having-large-disks)
- Unsupported restore configurations: ***Temp drive***, ***Deduplicated Disk*** and ***disk with write Accelerator enabled***. [Learn more](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support).
- [Post restore guidelines, example: Set up static IP, availability set, DC etc,..](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#post-restore-steps)
- UserErrorInvalidManagedDiskOperation -  Restore failed due to lack of Quota. [Learn more](https://docs.microsoft.com/azure/azure-portal/supportability/resource-manager-core-quotas-request)
- [UserErrorSkuNotAvaialable](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorskunotavailable---vm-creation-failed-as-vm-size-selected-is-not-available)
- [UserErrorMarketPlaceVMNotSupported](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrormarketplacevmnotsupported---vm-creation-failed-due-to-market-place-purchase-request-being-not-present)
- How to restore to latest or specific recovery point using [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#select-a-restore-point) or [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)
- [How to stop/cancel an ongoing restore job?](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#restore)
- Steps to restore using [Cross Region Restore](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#cross-region-restore)

Recommended Documents

- [Configure static IP address to restored VM](https://docs.microsoft.com/previous-versions/azure/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)<br>
- Attach an existing NIC to the restored VM:
   - Step 1: [Remove from original VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#remove-a-network-interface-from-a-vm)<br>
   - Step 2: [Attach to restored VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-add-nic)<br>
- [How to restore an encrypted VM when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault](https://docs.microsoft.com/azure/backup/backup-azure-restore-key-secret)
- [Restore a Domain Controller VM](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)<br>
- [Azure Virtual Machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [Supported/Unsupported configurations for restoring VM with management configuration changes](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-vm-management)
- [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#restore)
