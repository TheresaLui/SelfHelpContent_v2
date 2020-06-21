<properties
	pageTitle="UserErrorRestoreFailedDatabaseCannotBeOfflined"
	description="UserErrorRestoreFailedDatabaseCannotBeOfflined"
	infoBubbleText="Restore failed as the database could not be brought offline."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorrestorefaileddatabasecannotbeofflined"
	diagnosticScenario="azurebackup-crc-usererrorrestorefaileddatabasecannotbeofflined"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorRestoreFailedDatabaseCannotBeOfflined

<!--issueDescription-->
While doing a restore, the target database needs to be brought offline. Azure Backup is unable to bring this database offline.
<!--/issueDescription-->

## **Recommended Steps**

* Use the "additional details" in the Azure portal error menu to narrow down the root causes
* See the [Restore a Database Backup Using SSMS](https://docs.microsoft.com/sql/relational-databases/backup-restore/restore-a-database-backup-using-ssms?view=sql-server-2017) documentation for further troubleshooting
