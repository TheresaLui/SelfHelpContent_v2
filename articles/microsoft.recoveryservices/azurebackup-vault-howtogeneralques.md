<properties
	pageTitle="Vault How-to and general questions"
	description="Vault How-to and general questions"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632780"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="16bb11b7-571a-44fe-8534-b96eecb1296c"
	ownershipId="StorageMediaEdge_Backup"
/>

# Advisory questions related to Recovery Services Vault

Use the following guidelines when working with Recovery Services Vault

## **Recommended Documents**

**Delete a vault or Protected Items**<br>
You cannot delete a vault that contains protected data sources, backup data (active or in soft deleted state), or registered storage accounts.<br>
To delete the vault, refer to the following articles:
- [Step-by-step instructions to permanently delete the vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)<br>
- Check if soft deleted items are blocking vault delete and [learn how to disable it](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud#disabling-soft-delete-using-azure-portal)
- Determine whether backup infrastructure items are blocking vault delete by ensuring that no protected items are on the following path: <br>
     **Vault - Backup infrastructure** under **Protected Servers** and **Storage Accounts** tab. <br> 
See instructions on how to stop backup/protection for:
    * [Azure Virtual Machine](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)<br>
    * [SQL databases in Azure Virtual Machine](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#stop-protection-for-a-sql-server-database)<br>
    * [Azure File Share](https://docs.microsoft.com/azure/backup/manage-afs-backup#stop-protection-on-a-file-share)<br>
	
**Move a vault or backup data**
- [Change vault configuration from GRS to LRS ](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- [Move a vault between subscriptions](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription) and between [resource groups?](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group)<br>
- [Move backup data/protected items to another vault](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#can-i-move-backup-data-to-another-vault)<br>
- [Move data from the Recovery Services vault to on-premises](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#how-can-i-move-data-from-the-recovery-services-vault-to-on-premises)

**Cost, reports, and retention**
- [Azure Backup pricing information](https://azure.microsoft.com/pricing/details/backup/)
- [View cloud storage consumed at a backup-item level in Azure Backup reports](https://docs.microsoft.com/azure/backup/configure-reports#get-started)<br>
- [What happens to your existing and future recovery points if you modify policy](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#what-happens-when-i-change-my-backup-policy). See also [Impact of policy change on recovery points](https://docs.microsoft.com/azure/backup/backup-architecture#impact-of-policy-change-on-recovery-points)
- [Backup policy, schedule, and retention behaviour](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- Configure and monitor alerts and notification for a Vault using [Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor), [Azure monitor](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor) and [Backup Explorer](https://docs.microsoft.com/azure/backup/monitor-azure-backup-with-backup-explorer)

**Security**
- [How secure and reliable is Azure Backup infrastructure?](https://docs.microsoft.com/azure/backup/security-overview)
- [How to configure Private Endpoints for Azure Backup?](https://docs.microsoft.com/azure/backup/private-endpoints)
- [Encryption in Azure Backup](https://docs.microsoft.com/azure/backup/backup-encryption) and [using customer-managed keys](https://docs.microsoft.com/azure/backup/encryption-at-rest-with-cmk)

**Restore backup data**
- [Restore to create a new virtual machine](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)
- [Restore disks attached to the VM](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks)
- [Restore specific files within the VM](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)
- [Restore encrypted Azure virtual machines](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption)
- [Create a new VM or restore disks to a secondary region (Cross region restore to Azure paired region)](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#cross-region-restore)
- [Restore SQL Server databases on Azure VMs](https://docs.microsoft.com/azure/backup/restore-sql-database-azure-vm)
- Restore [files to Windows Server](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server) or [System State to Windows Server](https://docs.microsoft.com/azure/backup/backup-azure-restore-system-state) using the MARS Agent
