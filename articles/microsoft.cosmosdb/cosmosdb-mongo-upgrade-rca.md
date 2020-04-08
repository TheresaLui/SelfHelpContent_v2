<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v3.6"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v3.6"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-upgrade-rca"
    diagnosticScenario="CosmosDBMongoUpgradeInsight"
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to MongoDB API engine version 3.6

## Your database account, <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> qualifies to be updated to the latest version of Azure Cosmos DB's API for MongoDB.

<!--issueDescription-->
Upgrading to the latest version of the service will provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

<!--/issueDescription-->

The upgrade process will not provide any service interruptions or downtime. It will also not require any data or index migrations. As soon as you start the process, your account will be queued to proceed with the upgrade. You will be notified when your account has finished upgrading.

1. Benefits of upgrading to version 3.6

   - Enhanced performance and stability
   - Support for new database commands
   - Support for aggregation pipeline by default and new aggregation stages
   - Support for ChangeStream
   - Support for Compound Indexes
   - Cross-partition support for the following operations: UPDATE, DELETE, COUNT, and ORDER BY
   - Improved performance for the following aggregate operations: COUNT, SKIP, LIMIT, and GROUP BY

2. Changes from previous engine versions

   - MongoDB collections will only have the _id property indexed by default
   - Per request timeout is going to be 30 seconds
   - Recommended time to refresh idle connections is now 30 minutes

3. Action required

   The connection string to the MongoDB service in your application will need to be updated as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com` but it might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
