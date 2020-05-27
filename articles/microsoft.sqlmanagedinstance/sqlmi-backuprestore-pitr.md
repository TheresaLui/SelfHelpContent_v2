<properties
	pageTitle="Management/Backup a managed instance database"
	description="Management/Backup a managed instance database"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637234"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="14f2e3ce-48e0-4417-b4f1-5097ea71edf3"
	ownershipId="AzureData_AzureSQLMI"
/>
# Backup/Restore a managed instance database

Managed Instance takes [automatic backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to [restore a database to some point of time in past](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#point-in-time-restore) within the retention period or [restore accidentally deleted database](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285). Backups are kept 7 days by default and [this period can be increased up to 35 days](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups#how-to-change-the-pitr-backup-retention-period) ([10 year long-term retention](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-retention) is not still supported). Automated backups are charged since 11/01/2019. If you are experiencing some issues with automated backups or point-in-time restore operation, the following troubleshooting steps might help you to identify the issue.

## **Recommended Steps**

### Restore database (point in time restore)

- Find a database in the Azure portal and check the **earliest restore time value**. Check is the point-in time that you used after this time.
- If you cannot connect to the database that has completed restore, you might need to wait some additional time. The restored database must be registered in Azure, and in Business Critical tier, it should complete replication/seeding to all secondary replicas.
- Make sure that the account that is performing point-in-time restore has **Write** permission on Managed Instance and **Read** permission on subscription and resource group. The recommended role is [SQL Managed Instance Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-managed-instance-contributor).

### Automatic Backups

- If you want to check your backup storage cost, use [Azure Subscription Cost Analysis](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups#storage-costs)
- If you want to monitor automatic backup requests, [create an XEvent session](https://docs.microsoft.com/sql/relational-databases/backup-restore/back-up-and-restore-of-sql-server-databases#monitor-progress-with-xevent) that traces **sqlserver.backup_restore_progress_trace** event
- If you want to verify that recent automatic backups are completed, look at the error log or use [Azure Data Studio Managed instance extension](https://docs.microsoft.com/sql/azure-data-studio/azure-sql-managed-instance-extension#logs)
- If you want to track the progress of the ongoing automatic backup use [T-SQL to query Dynamic Management views](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=azuresqldb-mi-current#restore-mi-database-progress)
- If you cannot connect to the database that has completed restore, you might need to wait some additional time. The restored database must be registered in Azure, and in Business Critical tier, it should complete replication/seeding to all secondary replicas. 

## **Recommended Documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
