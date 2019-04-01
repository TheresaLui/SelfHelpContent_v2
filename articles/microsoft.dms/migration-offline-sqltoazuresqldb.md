<properties
	pageTitle="Errors for SQL Server to Azure SQLDB offline migration"
	description="Top 5 migration errors, what it means and what customer can do for SQL Server to Azure SQLDB offline migration"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="ajaykar"
	displayOrder="1"
	articleId="migration-offline-sqltoazuresqldb"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32615126"
	resourceTags=""
	productPesIds="16307"​
	cloudEnvironments="public"
/>

# <-- Errors you may encounter while migrating from SQL Server to Azure SQLDB using offline migration --> 

## **Top Errors - SQL Server to Azure SQLDB offline migration**

1. Could not start the scenario 'StartAzureSqlDbMigrationScenario' as an exception occurred while deserializing the input.<br>
<b>What it means:</b> If you hit this error it means that you provided a bad input through PowerShell.<br>
<b>What you can do:</b> Please review the input you provided.

2. Error 4060 - Login failed.<br>
<b>What it means:</b> Authentication failed with the target database.<br>
<b>What you can do:</b> Review user actions in <a href="https://docs.microsoft.com/en-us/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-2017">Authentication Errors Page</a> and take appropriate action.

3. Failed to start activity due to validation errors. Additional error information on column mismatch between source and target may be provided as well: <br>
&nbsp;&nbsp;a. The table in the source and target database needs to have the same number of non-computed columns.<br>
&nbsp;&nbsp;b. The nullability of column '<Column_name>' in table '<tablename>' is different on source and target.<br>
&nbsp;&nbsp;c. The data type of the column in the source table does not match with the data type in the target table.<br>
&nbsp;&nbsp;d. No columns found for the source table. It may not exist, it may have been deleted, or the user may not have access.<br>
<b>What it means:</b> The schema between source and target databases for a given table is not the same - DMS cannot migrate with mismatched schema. You may not have migrated the schema to the target, migrated incorrectly or schema changed in either source or target after you migrated the schema.<br>
<b>What you can do:</b> Make sure the schema on source and target is the same. Refer to select\deploy schema section in <a href="https://docs.microsoft.com/en-us/sql/dma/dma-migrateonpremsqltosqldb?view=sql-server-2017">SQL Server to Azure SQLDB Migration</a> if you need help.



## **Recommended documents**
[Tutorial: Migrate SQL Server to a single database or pooled database in Azure SQL Database offline using DMS](https://docs.microsoft.com/en-us/azure/dms/tutorial-sql-server-to-azure-sql)<br>
[Azure Database Migration Service Documentation](https://docs.microsoft.com/en-us/azure/dms/dms-overview)<br>
[Database Migration Guide](https://datamigration.microsoft.com/)
