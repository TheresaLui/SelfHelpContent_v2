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
	cloudEnvironments="public"
	articleId="14f2e3ce-48e0-4417-b4f1-5097ea71edf3"
/>
# Backup/Restore a managed instance database

Managed Instance takes automatic backups (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to restore a database to some point of time in past within the retention period or restore accidentally deleted database. For more information, see [Automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups). 

If you are experiencing some issues with automated backups or point-in-time restore operation, the following troubleshooting steps might help you to identify the issue.

## **Recommended steps**

### Restore database (point is time restore)

- Find a database in the Azure portal and check the `earliest restore time value`. Check is the point-in time that you used after this time.
- If you cannot connect to the database that has completed restore, you might need to wait some additional time. The restored database must be registered in Azure, and in Business Critical tier, it should complete replication/seeding to all secondary replicas.

### Automatic backups

- If you want to monitor automatic backup requests, create an XEvent session that traces `sqlserver.backup_restore_progress_trace` event.
- If you want to track the progress of the ongoing automatic backup use [T-SQL to query Dynamic Management views](https://docs.microsoft.com/sql/t-sql/statements/restore-statements-transact-sql?view=azuresqldb-mi-current#restore-mi-database-progress)
- If you cannot connect to the database that has completed restore, you might need to wait some additional time. The restored database must be registered in Azure, and in Business Critical tier, it should complete replication/seeding to all secondary replicas. 

## **Recommended documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)