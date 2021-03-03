<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for upgrade to v4.0"
    infoBubbleText="The customer's account is eligible for an upgrade to Azure Cosmos DB API for MongoDB v4.0"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-mongo-assistedupgrade-rca"
    diagnosticScenario="CosmosDBMongoAssistedUpgradeInsight"
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade to MongoDB Version 4.0

## Upgrade MongoDB API version

Your database account <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> can now be upgraded to the latest version of Azure Cosmos DB's API for MongoDB v4.0. Upgrading to the Mongo engine version 4.0 will provide the most up-to-date functionality, as well as enhancements in performance and stability.

The upgrade process will not result in any service interruptions nor require any downtime. It will require that you migrate the index by running the [reindex](https://docs.mongodb.com/manual/reference/method/db.collection.reIndex/) command on the identified collections. When the migration has completed, the account will show new connection strings in the Azure portal with `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.


### Benefits of upgrading to version 4.0

Version 4.0 includes the following new features:
- Support for multi-document transactions within unsharded collections.
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

- By default, the [Server Side Retry (SSR)](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors) feature is enabled. This means requests from the client application will not return 16500 errors. Instead, requests will resume until they complete or hit the 60 second timeout.
- Per request timeout is set to 60 seconds.
- MongoDB collections created on the new wire protocol version will only have the `_id` property indexed by default.

### Action required when upgrading from 3.2

When upgrading from 3.2, the database account endpoint suffix will be updated to the following format:

```
<your_database_account_name>.mongo.cosmos.azure.com
```

If you are upgrading from version 3.2, you'll need to replace the existing endpoint in your applications and drivers that connect with this database account. **Only connections that are using the new endpoint will have access to the features in the new API version**. The previous 3.2 endpoint should have the suffix `.documents.azure.com`.

>[!Note]
> This endpoint might have slight differences if your account was created in a Sovereign, Government, or Restricted Azure Cloud.

**Important Note:** Although 4.0 is generally compatible with 3.6 and 3.2, we recommend that you provision a new Cosmos DB account with MongoDB server version 4.0 to try it out with your application on a Dev or QA instance *before* you update your production application to use Mongo server version 4.0.

## **Recommended Documents**
- [Azure Cosmos DB API for MongoDB (4.0 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40)
- [Azure Cosmos DB API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
