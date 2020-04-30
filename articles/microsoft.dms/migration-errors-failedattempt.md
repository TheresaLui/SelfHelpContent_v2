<properties
	pageTitle="Migration activity failure"
	description="Migration activity failure"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="migration-errors-failedattempt"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673610,32673594,32673584"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseMigrationService"
/>

# Troubleshooting top common errors when running a migration activity  

## **Recommended Steps**

### Mongo DB to Cosmos DB Migration errors 

**Migration failing due to incorrect SSL Cert**

* Error: Remote certificate is invalid according to validation procedure
* Solution: [Use a certificate issued by a certificate authority](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account#connection-string-requirements)

**Unable to get the list of databases in DMS database setting blade**

* Cause: Storage account setting is missing the SAS info and thus cannot be authenticated
* Solution: [Create the SAS on the blob container using Storage Explorer and use the URL with the SAS for the container as the source connection string](https://docs.microsoft.com/azure/dms/tutorial-mongodb-cosmos-db#specify-source-details)

**Version of the database not supported when connecting to source**

* Cause: The version of the source database configured for migration is not supported by DMS yet. As newer versions of Mongo DB are released, they are tested with DMS to ensure compatibility and DMS is updated before they are supported as valid sources. 
* Workaround: In order to proceed with the migration before such update, export the databases/collections to Azure storage and use the "Data from Azure storage" option for source configuration as described [here](https://docs.microsoft.com/azure/dms/tutorial-mongodb-cosmos-db#specify-source-details)

### Migration Activity in Queued State

* [Troubleshooting migration activity in queued state](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#migration-activity-in-queued-state)<br>

## **Recommended Documents**

* [Troubleshoot common Azure DMS issues and errors](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)<br>
* [Known issues/migration limitations with online migrations to Azure SQL DB](https://docs.microsoft.com/azure/dms/known-issues-azure-sql-online)<br>
* [Known issues/migration limitations with online migrations to Azure DB for MySQL](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online)<br>
* [Known issues/migration limitations with online migrations to Azure DB for PostgreSQL](https://docs.microsoft.com/azure/dms/known-issues-azure-postgresql-online)
