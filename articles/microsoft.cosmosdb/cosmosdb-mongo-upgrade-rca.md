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
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to MongoDB API engine version 3.6

## Your database account, <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->, qualifies to be updated to the latest version of Azure Cosmos DB's API for MongoDB

<!--issueDescription-->
Upgrading to the latest version of the service will provide the most up-to-date functionality, the latest fixes, and enhancements in performance and stability.

<!--/issueDescription-->

<!--$DowntimeCondition-->[DowntimeCondition]<!--/$DowntimeCondition--> To start the upgrade, navigate to the **Settings** > **Features** area of your Cosmos DB Mongo account. You'll see the option Upgrade to Mongo server version 3.6. To start the migration, click the **Enable** button. You'll see **Pending** in the features list for up to several days. When the migration has completed, the account will show new connection strings in Azure Portal with `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.

**Note:** The notification might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

**Important Note:** Although 3.6 is generally compatible with 3.2, we recommend that you provision a new account through the portal and select the MongoDB server version 3.6 to try it out with the application on a dev or qa instance, before you update the account while backing any production workload.

1. Benefits of upgrading to version 3.6

   - Enhanced performance and stability
   - Support for new database commands
   - Support for aggregation pipeline by default and new aggregation stages
   - Support for ChangeStream
   - Support for Compound Indexes
   - Cross-partition support for the following operations: `UPDATE`, `DELETE`, `COUNT`, and `ORDER BY`
   - Improved performance for the following aggregate operations: `COUNT`, `SKIP`, `LIMIT`, and `GROUP BY`

2. Changes from previous engine versions

   - MongoDB collections will only have the `_id` property indexed by default
   - Per request timeout is going to be 60 seconds

3. Actions required

   - The connection string to the MongoDB service in your application will need to be updated, as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.

    **Note:** The endpoint might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

The previous connection string, with a `documents.azure.com` DNS suffix, will continue to be operational with the 3.2 server version until further notice. Your applications can be switched to the new connection string at your convenience.

## **Recommended Documents**

- [Azure Cosmos DB API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
