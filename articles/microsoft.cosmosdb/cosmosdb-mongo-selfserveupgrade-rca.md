<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v3.6"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v3.6"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-selfserveupgrade-rca"
    diagnosticScenario="CosmosDBMongoSelfServeUpgradeInsight"
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to Mongo server version 3.6

## Upgrade to Mongo server v3.6

Your database account <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> can now be upgraded to the latest version of Azure Cosmos DB's API for MongoDB v3.6. Upgrading to the Mongo engine version 3.6 will provide the most up-to-date functionality, as well as enhancements in performance and stability.

The upgrade process will not result in any service interruptions nor require any downtime. The existing data and indexes do not need to be migrated. [Select this blade](data-blade:Microsoft_Azure_DocumentDB.FeaturesBlade.id.$resourceId;data-blade-uri:{$domain}/#blade/Microsoft_Azure_DocumentDB/FeaturesBlade/id/{$resourceId}) to start the upgrade. You'll see the option, "Upgrade to Mongo server version 3.6". To start the migration, click the **Enable** button. You will see **Pending** status until your account has finished upgrading, which may take upto a day. When the migration has completed, the account will show new connection strings in Azure Portal with `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.

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

### Action required

The connection string to the MongoDB service in your application will need to be updated, as shown in the Overview dashboard of the Azure portal. The updated endpoint follows this format: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.

**Note:** The DNS suffix might differ if your account is in a Sovereign, Government, or Restricted Azure cloud. Please check the overview blade for your account on the Azure Portal.

The previous connection string with a `documents.azure.com` DNS suffix will continue to be operational with the 3.2 server version until further notice. You can switch your applications to the new connection string at your convenience.

**Important Note:** Although 3.6 is generally compatible with 3.2, we recommend that you provision a new Cosmos DB account with MongoDB server version 3.6 to try it out with your application on a Dev or QA instance **before you update your production application to use Mongo server version 3.6**.

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
