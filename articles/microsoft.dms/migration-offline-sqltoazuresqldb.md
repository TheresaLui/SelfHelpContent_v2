<properties
	pageTitle="Errors for SQL Server to Azure SQLDB offline migration"
	description="Top 5 migration errors, what it means and what customer can do for SQL Server to Azure SQLDB offline migration"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="ajaykar"
	ms.author="ajaykar"
	displayOrder="1"
	articleId="migration-offline-sqltoazuresqldb"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32615126"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public"
/>

# <-- Errors you may encounter while migrating from SQL Server to Azure SQLDB using offline migration --> 

## **Recommended Steps**

* **Error**: Could not start the scenario 'StartAzureSqlDbMigrationScenario' as an exception occurred while deserializing the input.

	This error displays when you have provided a bad input through PowerShell. Please review the input you provided.

* **Error 4060 - Login failed**

	Authentication has failed with the target database. Review user actions in [Authentication Errors Page](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-2017, and update authentication settings.

* **Error**: Failed to start activity due to validation errors.

	The schema between source and target databases for a given table is not the same - DMS cannot migrate with mismatched schema. You may not have migrated the schema to the target, migrated incorrectly or schema changed in either source or target after you migrated the schema. Make sure the schema on source and target is the same. Refer to the [SQL Server to Azure SQLDB Migration, select/deploy schema](https://docs.microsoft.com/sql/dma/dma-migrateonpremsqltosqldb?view=sql-server-2017). Additional error information on column mismatch between source and target may be provided as well:
	
	* The table in the source and target database needs to have the same number of non-computed columns
	* The nullability of column '<Column_name>' in table '<tablename>' is different on source and target
	* The data type of the column in the source table does not match with the data type in the target table
	* No columns found for the source table. It may not exist, it may have been deleted, or the user may not have access.
	
	
## **Recommended Documents**

* [Tutorial: Migrate SQL Server to a single database or pooled database in Azure SQL Database offline using DMS](https://docs.microsoft.com/azure/dms/tutorial-sql-server-to-azure-sql)<br>
* Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/dms-overview)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)
