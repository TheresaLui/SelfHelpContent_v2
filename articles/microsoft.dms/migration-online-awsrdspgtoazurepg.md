<properties
	pageTitle="Errors for AWS RDS PostgreSQL to Azure Database for PostgreSQL Online Migration"
	description="Top migration errors and troubleshooting info"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="3"
	articleId="migration-online-awsrdspgtoazurepg"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673576"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Configuration info for migrating from PostgreSQL to Azure Database for PostgreSQL using online migration and errors you may encounter while migrating 

## **Recommended Steps**

DMS offers migration from PostgreSQL source hosted on-premise or on AWS RDS to Azure Database for PostgreSQL. See tutorials for setting up migration under Recommended Documents below.

### Troubleshooting migration errors

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

* [Tutorial: Migrate PostgreSQL to Azure Database for PostgreSQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-postgresql-azure-postgresql-online)<br>
* [Tutorial: Migrate RDS PostgreSQL to Azure Database for PostgreSQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-rds-postgresql-server-azure-db-for-postgresql-online)
* [Azure Database for PostgreSQL Documentation](https://docs.microsoft.com/azure/postgresql)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)
