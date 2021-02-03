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

# Upgrade to Mongo server version 3.6

## Your database account <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> can now be upgraded to the latest version of Azure Cosmos DB's API for MongoDB (3.6).

<!--issueDescription-->
Upgrading to the Mongo engine version 3.6 will provide the most up-to-date functionality, as well as enhancements in performance and stability.
<!--/issueDescription-->

The upgrade process will not result in any service interruptions nor require any downtime. <!--$MigrationCondition-->[MigrationCondition]<!--/$MigrationCondition-->


**Benefits of upgrading to version 3.6**

    - Enhanced performance and stability
    - Support for new database commands
    - Support for aggregation pipeline by default and new aggregation stages
    - Support for ChangeStream
    - Support for Compound Indexes
    - Cross-partition support for the following operations: `update`, `delete`, `count`, and `sort`
    - Improved performance for the following aggregate operations: `$count`, `$skip`, `$limit`, and `$group`  


**Changes from previous engine versions**

    - New MongoDB collections created by you after migration will only have the `_id` property indexed by default.
    - Per request, timeout will be 60 seconds.  


**Action required**

The connection string to the MongoDB service in your application will need to be updated, as shown in the Overview dashboard of the Azure portal. The updated endpoint follows this format: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.


**Note:** The DNS suffix might differ if your account is in a Sovereign, Government, or Restricted Azure cloud. Please check the overview blade for your account on the Azure portal.

The previous connection string with a `documents.azure.com` DNS suffix will continue to be operational with the 3.2 server version until further notice. You can switch your applications to the new connection string at your convenience.

**Important Note:** Although 3.6 is generally compatible with 3.2, we recommend that you provision a new Cosmos DB account with MongoDB server version 3.6 to try it out with your application on a Dev or QA instance **before you update your production application to use Mongo server version 3.6**.


## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
