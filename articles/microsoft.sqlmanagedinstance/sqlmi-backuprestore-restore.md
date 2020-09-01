<properties
	pageTitle="Management/Restore a managed instance database"
	description="Management/Restore a managed instance database"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637256"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="b15059cf-640d-472e-887b-694eb3107c40"
	ownershipId="AzureData_AzureSQLMI"
/>
# Restore a managed instance database from Blob Storage

Managed Instance takes [automatic backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to [restore a database to some point of time in past](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#point-in-time-restore) within the retention period or [restore accidentally deleted database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285). Managed Instance also enables you to [restore a database from a backup file placed on Azure Blob Storage](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore), which is useful for migration from SQL Server. If you are experiencing some issues with any restore operation, the following troubleshooting steps might help you to identify the issue.

## **Recommended Steps**

- If you are noticing that some error is returned by **RESTORE**, check are you using [supported syntax in this statement](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#restore-statement)
- Check if there some [unsupported features](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#restore-statement) in your .bak file (for example, multiple log files or backup sets, too many database files or in-memory OLTP objects targeting General Purpose tier). Make sure that you are restoring full database backup (no **log backups**, **mdf** or **bacpac** files).
- Make sure that you are restoring **FULL** backup. If you need to restore differential or log backups, or perform online migration using Log Shipping use [Data Migration Service (DMS)](https://docs.microsoft.com/sql/dma/dma-overview). For bacpac and dacpac files use [SqlPackage](https://docs.microsoft.com/azure/sql-database/sql-database-import#import-from-a-bacpac-file-using-sqlpackage), SQL Server Management Studio, or Visual Studio SSDT. Attaching database **mdf** files is not supported.
- Make sure that you are restoring a database from **public blob storage** protected with **SAS credential**. [Private IPs for blob storage protected by firewall](https://docs.microsoft.com/azure/storage/common/storage-network-security) and service endpoints are currently not supported.
- Verify that you have created **CREDENTIAL** with the name equal to the URL of the blob storage where you want to backup your database. You can use part of [PowerShell script](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Automate-migration-to-Managed-Instance-using-PowerShell/ba-p/830801#M186) from the recommended documents to automate this process.
- Try to run **RESTORE FILELISTONLY** statement and check would Managed Instance return a list of the files in the backup
- If you cannot run **RESTORE FILELISTONLY**, check is your SAS credential placed in **SECRET** option of **CREATE CREDENTIAL** statement valid. The most common errors are the leading **?** in SAS token, expiry date **se** in past, valid date **sv** in future (due to time-zone difference), or **sp** (permission) not including **R** rights.
- If you are getting the error **33111** **Cannot find server certificate with thumbprint ...** make sure that you have [properly taken the backup of your TDE protected database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Take-a-backup-of-TDE-protected-database-on-Azure-SQL-Managed/ba-p/643407#M120)
- Script **CREDENTIAL** to SQL Server, and restore a database from Azure Blob Storage account the SQL Server
- If you want to track the progress of the ongoing **RESTORE** statement use [T-SQL to query Dynamic Management views](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=azuresqldb-mi-current#restore-mi-database-progress). The restored database might be shown in SSMS with random GUID instead of the database name while restore is in progress.
- If you believe that **RESTORE** progress is slow, make sure that Storage account is in the same region as Managed Instance, and that you have split backups on multiple URL. Using compressed backups can speed up your **RESTORE**.
- If you cannot connect to the database that has completed restore, you might need to wait some additional time. The restored database must be registered in Azure, and in Business Critical tier, it should complete replication/seeding to all secondary replicas.
- If you need to cancel the restore request, you would need to delete a database that you are restoring using [Azure PowerShell](https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabase?view=azps-2.1.0) or [Azure CLI](https://docs.microsoft.com/cli/azure/sql/midb?view=azure-cli-latest#az-sql-midb-delete).
- If you are getting the error **Stale/aborted version cleanup was aborted for database id '5' due to database shutdown.** make sure that you are [taking manual backups of databases on the managed instance with CHECKSUM enabled](https://docs.microsoft.com/azure/sql-database/sql-database-release-notes?tabs=single-database#restoring-manual-backup-without-checksum-might-fail).


## **Recommended Documents**

- [Restore a database in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
- [Automate migration to Managed Instance using PowerShell](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Automate-migration-to-Managed-Instance-using-PowerShell/ba-p/830801#M186)
