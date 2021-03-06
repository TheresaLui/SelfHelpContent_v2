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

**Restore scenarios**

- [What are the possible or best **restore options available**?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>
- Steps to restore using [Cross Region Restore](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#cross-region-restore)
- [How to restore disks](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks) and create a new VM using [ARM templates](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm), [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks), or [Azure CLI](https://docs.microsoft.com/azure/backup/tutorial-restore-disk)
- How to restore [selective disks](https://docs.microsoft.com/azure/backup/selective-disk-backup-restore#selective-disk-restore), [encrypted Azure VMs](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm), [selective files and folders](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-the-volume-and-copy-files)?
- If you can't find the files to restore, check unsupported restore configurations to see if the disks are backed up: ***Temp drive***, ***Deduplicated Disk***, ***Shared disk*** and disk with ***write Accelerator enabled***. [Learn more](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support)
- How to restore to latest or specific recovery point using [Portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#select-a-restore-point) or [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)
- [How to restore an encrypted VM when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) does not exist in the key vault](https://docs.microsoft.com/azure/backup/backup-azure-restore-key-secret)
- [Restore a Domain Controller VM](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)<br>

**Restore files**
- [Recovering files from an Encrypted Azure VM is currently not supported](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-file-level-restore). Alternatively, you can [restore disk of the encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm) and copy the required files
- [Guidelines to recover files from VM with large disk size(>4TB) and disk count(>16 disks)](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#virtual-machine-backups-having-large-disks)
- [How to restore files from Azure VM Backup?](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)
- Special restore configuration requirements for [Dynamic disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#dynamic-disks), [Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#windows-storage-spaces)

**Common restore issues**
- [Permissions/RBAC roles](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#before-you-start) required before performing a restore
- [How to stop/cancel an ongoing restore job?](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#can-i-cancel-an-in-progress-restore-job)

**Restore error codes**
- `UserErrorInvalidManagedDiskOperation` See [Restore failed due to lack of Quota](https://docs.microsoft.com/azure/azure-portal/supportability/resource-manager-core-quotas-request)
- [`UserErrorSkuNotAvailable`](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorskunotavailable---vm-creation-failed-as-vm-size-selected-is-not-available)
- [`UserErrorMarketPlaceVMNotSupported`](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrormarketplacevmnotsupported---vm-creation-failed-due-to-market-place-purchase-request-being-not-present)

## **Recommended Documents**

- [Supported/Unsupported configurations for restoring VM with management configuration changes](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-vm-management)
- [Post restore guidelines, example: Set up static IP, availability set, DC, and so on](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#post-restore-steps)
- [Configure static IP address to restored VM](https://docs.microsoft.com/previous-versions/azure/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)<br>
- Attach an existing NIC to the restored VM:
   - Step 1: [Remove from original VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#remove-a-network-interface-from-a-vm)<br>
   - Step 2: [Attach to restored VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-add-nic)<br>
- [Azure Virtual Machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#restore)
