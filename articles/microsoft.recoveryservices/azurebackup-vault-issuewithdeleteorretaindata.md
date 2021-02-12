<properties
	pageTitle="Issue with delete or retain data"
	description="Issue with delete or retain data"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632785"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0737d89c-41cb-471d-b2cb-e76d0de74c5f"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issue with delete or retain backed-up data

Use the following instructions to resolve issues with deleting or retaining backed-up data.

## **Recommended Steps**

**Retain data**

- How to stop backup/protection for:
	- [Azure Virtual Machine](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)<br>
	- [SQL databases in Azure Virtual Machine](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#stop-protection-for-a-sql-server-database)<br>
	- [Azure File Share](https://docs.microsoft.com/azure/backup/manage-afs-backup#stop-protection-on-a-file-share)<br>
- [What happens to my existing recovery points and future recovery points if I modify policy?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#what-happens-when-i-change-my-backup-policy)
- Impact of policy change on recovery points: [Azure VM](https://docs.microsoft.com/azure/backup/backup-architecture#impact-of-policy-change-on-recovery-points); [Azure file share](https://docs.microsoft.com/azure/backup/backup-azure-files-faq#what-is-the-impact-on-existing-recovery-points-and-snapshots-when-i-modify-the-backup-policy-for-an-azure-file-share-to-switch-from-daily-policy-to-gfs-policy) and [SAP HANA](https://docs.microsoft.com/azure/backup/sap-hana-faq-backup-azure-vm#impact-of-modifying-a-policy)
- [Backup policy, schedule, and retention behaviour](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)

**Delete vault**

You cannot delete a vault that contains protected data sources, contains backup data (active or in soft deleted state) or has registered storage accounts.<br>
To delete the vault refer to following articles:<br>

- [Step-by-step instructions to permanently delete the vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#proper-way-to-delete-a-vault)<br>
- Check if soft deleted items are blocking vault delete and [learn how to disable it](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud#disabling-soft-delete-using-azure-portal)
- Check if backup infrastructure items are blocking vault delete by ensuring there are no protected items on the following path: <br>
      **Vault - Backup infrastructure** under **Protected Servers** and **Storage Accounts** tab


## **Recommended Documents**

- [Why is the size of the data transferred to the Recovery Services vault smaller than the data selected for backup?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#why-is-the-size-of-the-data-transferred-to-the-recovery-services-vault-smaller-than-the-data-selected-for-backup)
- [If I cancel a backup job after it starts, is the transferred backup data deleted?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#if-i-cancel-a-backup-job-after-it-starts-is-the-transferred-backup-data-deleted)
- [Is there a limit on the amount of data backed up using a Recovery Services vault?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#is-there-a-limit-on-the-amount-of-data-backed-up-using-a-recovery-services-vault)
- [Delete old backup data from vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)
