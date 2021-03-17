<properties
		pageTitle="Azure Backup SQL Restore failures"
		description="Azure Backup SQL Restore failures"
		service="microsoft.recoveryservices"
		resource="vaults"
		authors="srinathv"
		ms.author="srinathv"
		displayOrder=""
		selfHelpType="generic"
		supportTopicIds="32605795"
		resourceTags=""
		productPesIds="15207"
		cloudEnvironments="public, fairfax, usnat, ussec"
		articleId="61978fe7-0f4c-44ab-b5f2-bc91c05dfeb8"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup SQL Restore failures

## **Recommended Steps**

- **Perform this step first:** To successfully restore SQL backup, ensure all the [prerequisites](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#prerequisites) are met
- Step-by-step instructions to [restore SQL DB](https://docs.microsoft.com/azure/backup/restore-sql-database-azure-vm) configured using Azure Backup

**Common error codes**
- [**UserErrorRestoreFailedDatabaseCannotBeOfflined** - Restore failed because the database could not be brought offline](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorrestorefaileddatabasecannotbeofflined)</br>
- [**UserErrorCannotRestoreExistingDBWithoutForceOverwrite** - Database with same name already exists at the target location](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorcannotrestoreexistingdbwithoutforceoverwrite)<br>
- [**UserErrorCannotFindServerCertificateWithThumbprint** - Cannot find the server certificate with thumbprint on the target](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorcannotfindservercertificatewiththumbprint)<br>

## **Recommended Documents**

- [FAQ for SQL Server backup](https://docs.microsoft.com/azure/backup/faq-backup-sql-server)<br>
- [Troubleshooting restore issues for backing up SQL Server on Azure](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot)<br>
