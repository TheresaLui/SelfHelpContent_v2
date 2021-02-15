<properties
	pageTitle="usererrorbackupfailedstandalonedatabasemovedintoag"
	description="usererrorbackupfailedstandalonedatabasemovedintoag"
	infoBubbleText="SQL database does not exist."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupfailedstandalonedatabasemovedintoag"
	diagnosticScenario="azurebackup-crc-usererrorbackupfailedstandalonedatabasemovedintoag"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBackupFailedStandaloneDatabaseMovedInToAG

<!--issueDescription-->
This error occurs if the database was initially protected as a standalone database, but was later made a part of the Always On availability group.
<!--/issueDescription-->

## **Recommended Steps**

- For the backups to continue successfully, remove the database from the Always On availability group. However, if you want to protect the database as a part of the availability group do: 
 - Step 1: [Stop backup with retain data](https://docs.microsoft.com/azure/backup/manage-monitor-sql-database-backup#stop-protection-for-a-sql-server-database)
 - Step 2: Re-discover the database and re-trigger [Configure backup](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#discover-sql-server-databases) operation on it.
