<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v4.0"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v4.0"
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

# Upgrade to Mongo server version 4.0

## Migrate to Azure Cosmos DB API for MongoDB v4.0

Migrate your database account, `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->` to a new database account to take advantage of the latest version of Azure Cosmos DB's API for MongoDB v4.0. This version provides the most up-to-date functionality, as well as enhancements in performance and stability.

When upgrading the service, you must also migrate the data in your existing account to a new account created using version 4.0 of the MongoDB API engine. Azure Data Factory or Studio 3T can assist you in migrating your data.

## Upgrading to 4.0 or 3.6

### Benefits of upgrading to version 4.0

Version 4.0 includes the following new features:

- Support for multi-document transactions within unsharded collections
- New aggregation operators
- Enhanced scan performance
- Faster, more efficient storage

### Benefits of upgrading to version 3.6

Version 3.6 includes the following new features:

- Enhanced performance and stability
- Support for new database commands
- Support for aggregation pipeline by default and new aggregation stages
- Support for Change Streams
- Support for compound Indexes
- Cross-partition support for the following operations: update, delete, count and sort
- Improved performance for the following aggregate operations: $count, $skip, $limit and $group
- Wildcard indexing is now supported

### Changes from version 3.2

- By default, the [Server Side Retry (SSR)](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors) feature is enabled, so that requests from the client application will not return 16500 errors. Instead, requests will resume until they complete or hit the 60-second timeout.
- Per request timeout is set to 60 seconds
- MongoDB collections created on the new wire protocol version will only have the `_id` property indexed by default

## **Recommended Documents**

- Learn more about the [supported and unsupported features of MongoDB version 4.0](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40).
- Learn more about the [supported and unsupported features of MongoDB version 3.6](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36).
- Learn more about [server-side retries](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors).
- [Migrate your data with Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
