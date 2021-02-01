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

# Upgrade to MongoDB API engine version 3.6

## Advantages of upgrading to MongoDB API engine V 3.6.

To take advantage of the latest version of the Azure Cosmos DB API for your MongoDB database account, you must migrate <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> to a new database account.

<!--issueDescription-->

Version 3.6 of the service provides the most up-to-date functionality, recent fixes, and enhancements in performance and stability.

<!--/issueDescription-->

When upgrading the service, you must also migrate the data in your existing account to a new account created using version 3.6 of the MongoDB API engine. Azure Data Factory or Studio 3T can assist you in migrating your data.

1. Benefits of upgrading to version 3.6 include:

   - Enhanced performance and stability
   - Support for new database commands
   - Support for aggregation pipeline by default and new aggregation stages
   - Support for ChangeStream
   - Support for Compound Indexes
   - Cross-partition support for the following operations: `UPDATE`, `DELETE`, `COUNT`, and `ORDER BY`
   - Improved performance for the following aggregate operations: `COUNT`, `SKIP`, `LIMIT`, and `GROUP BY`

2. Changes from previous engine versions include:

   - MongoDB collections have only the `_id` property indexed by default
   - Per request, timeout is 60 seconds

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
- [Migrate your data with Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
