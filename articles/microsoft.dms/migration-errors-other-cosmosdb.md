<properties
	pageTitle="Other Migration Issues to Azure CosmosDB"
	description="Other Migration Issues"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-other-cosmosdb"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743207"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting top common errors when running a migration activity  

## **Recommended Steps**

### MongoDB to Cosmos DB Migration errors 

**Migration failing due to incorrect SSL Cert**

* Error: Remote certificate is invalid according to validation procedure
* Solution: [Use a certificate issued by a certificate authority](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account#connection-string-requirements)

**Unable to get the list of databases in DMS database setting blade**

* Cause: Storage account setting is missing the SAS info and thus cannot be authenticated
* Solution: [Create the SAS on the blob container using Storage Explorer and use the URL with the SAS for the container as the source connection string](https://docs.microsoft.com/azure/dms/tutorial-mongodb-cosmos-db#specify-source-details)

**Version of the database not supported when connecting to source**

* Cause: The version of the source database configured for migration is not supported by DMS yet. As newer versions of MongoDB are released, they are tested with DMS to ensure compatibility and DMS is updated before they are supported as valid sources. 
* Workaround: In order to proceed with the migration before such update, export the databases/collections to Azure storage and use the "Data from Azure storage" option for source configuration as described [here](https://docs.microsoft.com/azure/dms/tutorial-mongodb-cosmos-db#specify-source-details)

## Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>

## **Recommended Documents**

* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>

## Troubleshooting the error when more than max number of databases are selected for migration  

## **Recommended Steps**

* [Troubleshooting max number of databases selected for migration](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#max-number-of-databases-selected-for-migration)
* **Error**: "Service has reported errors when trying to migrate more than 4DBs per service."

	* The Service can only migrate 4 DBs concurrently and you can have 2 services per subscription
	* DMS only supports 4 DBs to migrate concurrently. It allows you to create many projects, for example, you create 10 projects and select 4 databases in each. Although you have 40 Dbs but only 4 of them will be migrated at one time.
	* Another limit is per sub, per region, only 2 DMS services are allowed to create, which means you will have 8 Dbs to migrate concurrently at one time

