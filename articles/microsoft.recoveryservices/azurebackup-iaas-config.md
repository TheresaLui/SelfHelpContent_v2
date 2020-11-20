<properties
	pageTitle="Azure IAAS VM Backup Configure Protection"
	description="Azure IAAS VM Backup Configure Protection failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	ms.author="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553285"
	resourceTags=""
	productPesIds="15207"
	articleId="95333929-5668-4cb5-bed3-3855436ddbf7"
	cloudEnvironments="public, fairfax, usnat, ussec"
		ownershipId="StorageMediaEdge_Backup"
/>

# Unable to Configure Backup for Azure Virtual Machines

## **Recommended Documents**

To self resolve some of the common configuration issues, follow these instructions.

**Configuring backup**
- [How do I take multiple backups on the same day?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup) **Scheduled backup** is limited to one per day, for multiple backups use on-demand backup as workaround. 
- How to troubleshoot [permission issues during configure protection](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault) (or) [Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- How to configure protection through [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation) and [Azure automation](https://docs.microsoft.com/azure/backup/backup-rm-template-samples)
- [How to configure backup of Azure VM from a Recovery Service vault?](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare)
- If your VM is not listed to configure backup, then it might be soft deleted state [Learn more](https://docs.microsoft.com/azure/backup/soft-delete-virtual-machines#soft-delete-for-vms-using-azure-portal).  
- [Can I exclude disks that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)
- Unsupported Backup configurations: ***Shared disk***, ***Temp drive***, ***Deduplicated Disk***, ***Ultra disk*** and ***disk with write Accelerator enabled***. [Learn more](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support)<br>

**Moving resources**

- [How do I change my vault storage replication type from **GRS to LRS**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- How to move:  Azure VM across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group)/VM across [Vault](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#move-an-azure-virtual-machine-to-a-different-recovery-service-vault); Vault across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group)/Vault across [Subscription](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)<br>
- **Moving Recovery points/backup data** across Vaults/Subscription is not supported. <br>

**Disable backup**

- [How long will the backup data be retained after I stop backup?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- [How to **stop protecting a virtual machine** with retain backup data (or) delete backup data?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)<br>


**Delete backups/vault**

- [How to delete a Recovery Services vault?](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)<br>
- Cannot delete recovery service vault?, Ensure there are [no protected items](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#delete-protected-items-in-the-cloud) and there are [no soft-deleted items](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud) in the vault
- [How to delete VM that is in **soft delete state**?](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud)<br>
- [How to delete Backup data?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#delete-backup-data)<br>


## **Recommended documents**

- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- How to enable backup [during VM creation](https://docs.microsoft.com/azure/backup/backup-during-vm-creation) (or) [after creating a VM](https://docs.microsoft.com/azure/backup/backup-during-vm-creation#start-a-backup-after-creating-the-vm)
- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
