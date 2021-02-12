<properties
	pageTitle="Other Migration Issues to Azure PostgreSQL"
	description="Other Migration Issues"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-other-postgres"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743209"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting migration errors

**Migration errors - AWS RDS PostgreSQL to Azure Database for PostgreSQL using online migration**

* **Error**: The Default value of column '{column}' in table '{table}' in database '{database}' is different on source and target servers. It's '{value on source}' on source and '{value on target}' on target.

	This errors occurs when the default value on a column schema is different on source and target databases. Please make sure schema on the target matches schema on the source. If you need help with migrating schema, please refer to our [Azure PostgreSQL online migration documentation](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#migrate-the-sample-schema).

* **Error**: Target database '{database}' has '{number of tables}' tables where as source database '{database}' has '{number of tables}' tables. The number of tables on source and target databases should match.

	This errors occurs when the number of tables are different on source and target databases. Please make sure schema on the target matches schema on the source. If you need help with migrating schema, please refer to our [Azure PostgreSQL online migration documentation](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#migrate-the-sample-schema).

* **The source database {database} is empty**

	This errors occurs when the source database is empty. This is most likely because you have selected the wrong database as source. Please recheck the source database you selected for migration. 

* **The target database {database} is empty.** Please migrate the schema.

	This errors occurs when there is no schema on the target database. Please make sure schema on the target matches schema on the source. If you need help with migrating schema, please refer to our [Azure PostgreSQL online migration documentation](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online#migrate-the-sample-schema).

## **Recommended Documents**

* [Known issues/migration limitations with online migrations to Azure DB for PostgreSQL](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online)
* [Tutorial: Migrate PostgreSQL to Azure Database for PostgreSQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online)<br>
* [Tutorial: Migrate RDS PostgreSQL to Azure Database for PostgreSQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-rds-postgresql-server-azure-db-for-postgresql-online)
* [Azure Database for PostgreSQL Documentation](https://docs.microsoft.com/azure/postgresql)<br>
* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/)
* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)

## Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>

## Troubleshooting the error when more than max number of databases are selected for migration  

## **Recommended Steps**

* [Troubleshooting max number of databases selected for migration](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#max-number-of-databases-selected-for-migration)
* **Error**: "Service has reported errors when trying to migrate more than 4DBs per service."

	* The Service can only migrate 4 DBs concurrently and you can have 2 services per subscription
	* DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
	* Another limit is per sub, per region, only 2 DMS services are allowed to create, which means you will have 8 Dbs to migrate concurrently at one time
