<properties
	pageTitle="Planning and Configuration for Migration to MySQL"
	description="Planning and Configuration"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="planning-config-mysql"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743214"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Configuration info for migrating from MySQL to Azure Database for MySQL using online migration and errors you may encounter while migration

## **Recommended Steps**

DMS offers migration from a MySQL (RDS and non-RDS) source to a MySQL (Azure) target. For the configuration info, please visit their respective links below under Recommended documents.

For both scenarios, please follow the "Prerequisites" section. There, you will need to modify the needed parameters to aid in a migration. 

After you set up the prerequisites, please make sure you migrate the schema for the data migration. DMS requires a schema copy of the source on the target prior to starting the data migration - you may need to make modifications to it, however. Please follow the steps in the "Migrate the [sample] schema" section in the respective links provided for guidance on how to migrate the schema and on what modifications may be needed. 


## **Recommended Documents**

* [Tutorial: Migrate MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)<br>
* [Tutorial: Migrate RDS MySQL to Azure Database for MySQL online using DMS](https://docs.microsoft.com/azure/dms/tutorial-rds-mysql-server-azure-db-for-mysql-online)<br>
* [Azure Database for MySQL Documentation](https://docs.microsoft.com/azure/mysql)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)