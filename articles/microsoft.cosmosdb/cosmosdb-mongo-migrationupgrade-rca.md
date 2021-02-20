<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v3.6"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v3.6"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-migrationupgrade-rca"
    diagnosticScenario=""
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to Mongo server version 3.6

## Migrate to Azure Cosmos DB API for MongoDB v3.6

Migrate <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> to a new database account to take advantage of the latest version of the Azure Cosmos DB API for MongoDB v3.6. This version provides the most up-to-date functionality, recent fixes, and enhancements in performance and stability.

When upgrading the service, you must also migrate the data in your existing account to a new account created using version 3.6 of the MongoDB API engine. Azure Data Factory or Studio 3T can assist you in migrating your data.

### Benefits of upgrading to version 3.6

- Enhanced performance and stability
- Support for new database commands
- Support for aggregation pipeline by default and new aggregation stages
- Support for Change Streams
- Support for compound indexes
- Cross-partition support for the following operations: `update`, `delete`, `count`, and `sort`
- Improved performance for the following aggregate operations: `$count`, `$skip`, `$limit`, and `$group`
- Wildcard indexing is now supported

### Changes from previous engine versions

- **RequestRateIsLarge errors have been disabled by default**. Requests from the client application will not return 16500 errors anymore. Instead requests will resume until they complete or fulfill the timeout. Disabling server-side retries will restore the old behavior.
- Per request timeout is set to 60 seconds.
- MongoDB collections created on the new wire protocol version will only have the `_id` property indexed by default.

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB v3.6](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
- [Migrate your data with Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
