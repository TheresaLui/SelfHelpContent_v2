<properties
	pageTitle="Other Migration Issues to Azure SQL DB Managed Instance"
	description="Other Migration Issues for Azure SQL DB Managed Instance"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-other-sqldbmi"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743211"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting migration failures 

See How-to Guides, Tutorials and Resources section in Azure Database Migration Service Documentation website for DMS prerequisites, service instance, configuring migration projects, and troubleshooting errors.

## **Recommended Documents**

* [Azure Database Migration Service Documentation](https://docs.microsoft.com/azure/dms/)
* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>
* [Database Migration Guide](https://datamigration.microsoft.com/)

## Troubleshooting the error when more than max number of databases are selected for migration  

## **Recommended Steps**

* [Troubleshooting max number of databases selected for migration](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#max-number-of-databases-selected-for-migration)
* **Error**: "Service has reported errors when trying to migrate more than 4DBs per service."

	* The Service can only migrate 4 DBs concurrently and you can have 2 services per subscription
	* DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
	* Another limit is per sub, per region, only 2 DMS services are allowed to create, which means you will have 8 Dbs to migrate concurrently at one time

## Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>
