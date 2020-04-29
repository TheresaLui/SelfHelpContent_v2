<properties
	pageTitle="Management/Back up a managed instance database"
	description="Management/Back up a managed instance database to Azure Blob Storage"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637314"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="b951b1c5-2d93-4c5a-8fc6-836421bda563"
	ownershipId="AzureData_AzureSQLMI"
/>
# Back up a managed instance database to Azure Blob Storage

Managed Instance enables you to manually make a **COPY_ONLY** backups of a database to Azure Blob Storage using Transact-SQL **BACKUP TO URL** statement. These backups are not [automatic managed backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to [restore a database to some point of time in past](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#point-in-time-restore) within the retention period or [restore accidentally deleted database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285). If you are experiencing some issues with manual backup operation, the following troubleshooting steps might help you to identify the issue.

## **Recommended Steps**

- If you are noticing that some error is returned by **BACKUP** T-SQL statement, check are you using [supported syntax in this statement](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#backup) (for example mandatory **COPY_ONLY** option, no differential and log backups)
- If you cannot backup a database due to error **33111 Cannot find server certificate with thumbprint ...** check is it protected with Transparent Data Encryption (TDE). You need to [disable TDE protection in order to take a manual backup](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Take-a-backup-of-TDE-protected-database-on-Azure-SQL-Managed/ba-p/643407#M120).
- Verify that you have created **CREDENTIAL** with the name equal to the URL of the blob storage where you want to backup your database that has at least **rw** permission in SAS token. You can use PowerShell in the article below to setup Azure Storage account and create valid SAS tokens.
- Make sure that you have valid type of Azure Storage account (for example -SkuName Standard_LRS -Kind StorageV2)
- Script **CREDENTIAL** and backup a database from the SQL Server to Azure Blob Storage account
- Check is your SAS credential placed in **SECRET** option of **CREATE CREDENTIAL** statement valid. The most common errors are leading *?* in SAS token, wrong *se* (expiry date), *st* (start date),*sp* (permission) property. 
- Check is your database greater than 195GB and are you using in this scenario multiple URL stripes so every stripe would be less than 195 GB. Maximal backup stripe size on Azure Blob Storage can be 195 GB.
- If you are getting the errors **3063** or **3202** add the following options in the `BACKUP` statement: `MAXTRANSFERSIZE=4194304`, `BLOCKSIZE=65536`, and `COMPRESS`
- If you want to track the progress of the ongoing **BACKUP** statement use [T-SQL to query Dynamic Management views](https://docs.microsoft.com/sql/t-sql/statements/backup-transact-sql?view=azuresqldb-mi-current6#backup_progress)

## **Recommended Documents**

- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
- [Take a backup of TDE protected database on Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Take-a-backup-of-TDE-protected-database-on-Azure-SQL-Managed/ba-p/643407#M120)
- [Automate migration to Managed Instance using PowerShell](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Automate-migration-to-Managed-Instance-using-PowerShell/ba-p/830801#M186)
