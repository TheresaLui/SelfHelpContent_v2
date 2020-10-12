<properties
	pageTitle="Other Migration Issues to Azure SQL DB"
	description="Other Migration Issues"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-other-sqldb"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743210"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting errors while migrating to Azure SQLDB

## Errors you may encounter while migrating from SQL Server to Azure SQLDB using offline migration  

## **Recommended Steps**

* **Error**: Could not start the scenario 'StartAzureSqlDbMigrationScenario' as an exception occurred while deserializing the input.

	This error displays when you have provided a bad input through PowerShell. Please review the input you provided.

* **Error 4060 - Login failed**

	Authentication has failed with the target database. Review user actions in [Authentication Errors Page](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-2017), and update authentication settings.

* **Error**: Failed to start activity due to validation errors.

	The schema between source and target databases for a given table is not the same - DMS cannot migrate with mismatched schema. You may not have migrated the schema to the target, migrated incorrectly or schema changed in either source or target after you migrated the schema. Make sure the schema on source and target is the same. Refer to the [SQL Server to Azure SQLDB Migration, select/deploy schema](https://docs.microsoft.com/sql/dma/dma-migrateonpremsqltosqldb?view=sql-server-2017). Additional error information on column mismatch between source and target may be provided as well:
	
	* The table in the source and target database needs to have the same number of non-computed columns
	* The nullability of column '<column_name>' in table '<table_name>' is different on source and target
	* The data type of the column in the source table does not match with the data type in the target table
	* No columns found for the source table. It may not exist, it may have been deleted, or the user may not have access.


## **Recommended Documents**

* [Tutorial: Migrate SQL Server to a single database or pooled database in Azure SQL Database offline using DMS](https://docs.microsoft.com/azure/dms/tutorial-sql-server-to-azure-sql)<br>
* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/dms-overview)
* [Database Migration Guide](https://datamigration.microsoft.com/)

## Errors you may encounter while migrating from AWS RDS SQL Server to Azure SQL Database using online migration

## **Recommended Steps**

**Migration errors - AWS RDS SQL Server to Azure SQL Database using online migration**

* **CDC is not enabled for database {0} and table {1}**, which is a required setting for performing continuous sync. 

	This error happens when Change Data Capture (CDC) is not enabled for tables in your source database. This is required if you want to use continuous sync (online migration) for migrating your database to Azure. Please refer to [How to enable Change Data Capture](https://docs.microsoft.com/sql/relational-databases/track-changes/enable-and-disable-change-data-capture-sql-server?view=sql-server-2017) on how to enable this for your source database and tables within.
	
	To check if there are any user tables that do not have CDC enabled use the query below:

```
USE '{0}'; SELECT is_tracked_by_cdc, name AS TableName FROM sys.tables WHERE type = 'U' AND is_ms_shipped = 0 AND OBJECTPROPERTY(OBJECT_ID, 'TableHasPrimaryKey') = 0;
```

If the results show 'is_tracked_by_cdc' as 0 for one or more tables, enable the change capture for the database and for the specific tables.

* **Full Backup is not taken for database {0}**, this is needed to perform replicate features for continuous sync. 
	
	This error occurs when the service cannot find source database backups. Full source database backup is required to perform replicate features for continuous sync. You can refer to [How to create a full database backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/create-a-full-database-backup-sql-server?view=sql-server-2017) for more details.

	You can use the below query to check if Full database backups were taken on the source database(s):

```
SELECT COUNT(type) AS result FROM msdb.dbo.backupset bk WHERE bk.database_name = '{0}' AND type = 'D'
```


* **The recovery model of the database {0} is neither Full nor Bulk**, which is a required setting for performing continuous sync. 

	This error happens when the recovery model of your source database is not set to Full or Bulk. This is required if you want to use continuous sync (online migration) for migrating your database to Azure. You can [view or change the current recovery model of your source database](https://docs.microsoft.com/sql/relational-databases/backup-restore/view-or-change-the-recovery-model-of-a-database-sql-server?view=sql-server-2017) by following the below steps:

	* Connect to the source SQL Server using Microsoft SQL Server Management Studio
	* From the Standard bar, click New Query
	* Copy and paste the following query and Execute. This example shows how to query the sys.databases catalog view to learn the recovery model of the database: `SELECT name, recovery_model_desc FROM sys.databases WHERE name = '{0}'; GO`
	* If the result shows 'SIMPLE' recovery mode, change the database recovery mode to 'FULL' using this T-SQL command: `USE master; ALTER DATABASE {0} SET RECOVERY FULL;`
	* Take Full database backup after the recovery mode is changed to FULL

## **Recommended Documents**

* [Tutorial: Migrate RDS SQL Server to Azure SQL Database online using DMS](https://docs.microsoft.com/azure/dms/tutorial-rds-sql-server-azure-sql-and-managed-instance-online)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)

## Troubleshooting migration failures 

See How-to Guides, Tutorials and Resources section in Azure Database Migration Service Documentation website for DMS pre-requisites, service instance, configuring migration projects, and troubleshooting errors.

## **Recommended Documents**

* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/)
* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>
* [Known issues/migration limitations with online migrations to Azure SQL DB](https://docs.microsoft.com/azure/dms/known-issues-azure-sql-online)<br>

## Troubleshooting the error when more than max number of databases are selected for migration  

## **Recommended Steps**

* [Troubleshooting max number of databases selected for migration](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#max-number-of-databases-selected-for-migration)
* **Error**: "Service has reported errors when trying to migrate more than 4DBs per service."

	* The Service can only migrate 4 DBs concurrently and you can have 2 service per subspcription
	* DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
	* Another limit is per sub, per region, only 2 DMS services are allowed to create, which means you will have 8 Dbs to migrate concurrently at one time

## Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>
