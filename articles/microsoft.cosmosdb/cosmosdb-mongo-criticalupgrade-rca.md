<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v3.6"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v3.6"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-criticalupgrade-rca"
    diagnosticScenario="CosmosDBMongoCriticalUpgradeInsight"
    selfHelpType="rca"
    supportTopicIds="32636766, 32636771, 32636778, 32636784, 32636789, 32738475, 32636819, 32636831"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to MongoDB API engine version 3.6

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Upgrading to the latest version of Azure Cosmos DB's API for MongoDB will help you resolve the issues that you encounter and will provide the most up-to-date functionality, the latest fixes, and enhancements in performance and stability.

<!--/issueDescription-->

You may experience service interruptions or downtime during the upgrading process. This process may also require data or index migrations. We will proceed with the upgrade only with your consent, at a time convenient for you. As soon as you start the process, your account will be queued to proceed with the upgrade. You will be notified when your account has finished upgrading.

1. Benefits of upgrading to version 3.6

   - Enhanced performance and stability
   - Support for new database commands
   - Support for aggregation pipeline by default and new aggregation stages
   - Support for ChangeStream
   - Support for Compound Indexes
   - Cross-partition support for the following operations: `UPDATE`, `DELETE`, `COUNT`, and `ORDER BY`
   - Improved performance for the following aggregate operations: `COUNT`, `SKIP`, `LIMIT`, and `GROUP BY`

2. Changes from previous engine versions

   - MongoDB collections will have only the `_id` property indexed by default
   - Per request timeout will be 60 seconds

3. Actions required

   The connection string to the MongoDB service in your application will need to be updated, as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com` 

   **Note:** The endpoint might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

The previous connection string, with a `documents.azure.com` DNS suffix, will continue to be operational with the 3.2 server version until further notice. Your applications can be switched to the new connection string at your convenience.

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
