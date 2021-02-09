<properties
	pageTitle="Unable to delete vault"
	description="Issue with delete vault"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632791"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ac99254c-7320-4261-8c2b-3bea2a1a0022"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with delete vault

## **Recommended Steps**

You cannot delete a vault that contains protected data sources, contains backup data (active or in soft deleted state) or has registered storage accounts. To delete the vault refer to below articles:<br>

- [Step-by-step instructions to permanently delete the vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)<br>
- Check if soft deleted items are blocking vault delete and [learn how to disable it](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud#disabling-soft-delete-using-azure-portal)
- Check if backup infrastructure items are blocking vault delete by ensuring that no protected items are on the following path: <br>
     **Vault - Backup infrastructure** under **Protected Servers** and **Storage Accounts** tab

## **Recommended Documents**
- How to stop backup/protection for:
	- [Azure Virtual Machine](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
	- [SQL databases in Azure Virtual Machine](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#stop-protection-for-a-sql-server-database)
	- [Azure File Share](https://docs.microsoft.com/azure/backup/manage-afs-backup#stop-protection-on-a-file-share)
