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

## **Recommended Steps**

* Deletion Failed: There are backup items associated with the server. Stop protection and [delete backups for each of the backup items](https://aka.ms/DeleteBackupItems) to delete the server's registration. If the issue persists, contact support.
	
* Navigate to your on-premises server Management Console (MARS, Azure Backup Server or SC DPM depending on where your back items are protected) and perform the steps listed in [Deleting backup items from management console](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault#deleting-backup-items-from-management-console)

## **Recommended Documents**

- [Why is the size of the data transferred to the Recovery Services vault smaller than the data selected for backup?](https://aka.ms/AB-smaller-data-backup)<br>
- [If I cancel a backup job after it starts, is the transferred backup data deleted?](https://aka.ms/AB-transferred-backup-data)<br>
- [Is there a limit on the amount of data backed up using a Recovery Services vault?](https://aka.ms/AB-data-backed-up)<br>
- [Delete old backup data from vault](https://aka.ms/AB-retain-the-data)<br>
- [Determine the data source size](https://aka.ms/aka.msAB-data-source-size)<br>
