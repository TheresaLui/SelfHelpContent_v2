<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade eligibility RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account eligible for self-serve upgrade to v4.0"
    infoBubbleText="The customer's account is eligible for a self-serve upgrade to Azure Cosmos DB API for MongoDB v4.0"
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

# Upgrade MongoDB API Version

## Upgrade to MongoDB API version 4.0

Your database account, `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->` can now be upgraded to the latest version of Azure Cosmos DB's API for MongoDB v4.0. Upgrading will provide the most up-to-date functionality, as well as enhancements in performance and stability.

The upgrade process will not result in any service interruptions nor require any downtime. The existing data and indexes do not need to be migrated.

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

- By default, the [Server Side Retry (SSR)](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors) feature is enabled, so that requests from the client application will not return 16500 errors. Instead requests will resume until they complete or hit the 60 second timeout.
- Per request timeout is set to 60 seconds
- MongoDB collections created on the new wire protocol version will only have the `_id` property indexed by default

### Action required when upgrading from 3.2

When upgrading from 3.2, the database account endpoint suffix will be updated to the following format: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com`.

If you are upgrading from version 3.2, you'll need to replace the existing endpoint in your applications and drivers that connect with this database account. **Only connections that are using the new endpoint will have access to the features in the new API version**. For reference, the previous 3.2 endpoint is `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.documents.azure.com`. This endpoint might have slight differences if your account was created in a Sovereign, Government, or Restricted Azure Cloud.

## How to upgrade

1. Go to the Azure portal and navigate to your Azure Cosmos DB API for MongoDB account **Overview** blade. Verify that your current server version is what you expect.

2. From the options on the left, select the **Features** blade. This will reveal the Account level features that are available for your database account. Alternatively, click [here](data-blade:Microsoft_Azure_DocumentDB.FeaturesBlade.id.$resourceId;data-blade-uri:{$domain}/#blade/Microsoft_Azure_DocumentDB/FeaturesBlade/id/{$resourceId}) to directly navigate to the **Features** blade for your account.

3. Select the `Upgrade Mongo server version` row. If you don't see this option, your account might not be eligible for this upgrade. If this is the case, file [a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade).

4. Review the information displayed about the upgrade. When you're ready to start the process, select `Enable`. After you start the process, the `Features` menu will show the status of the upgrade. Status will go from `Pending`, to `In Progress`, to `Upgraded`. This process will not affect the existing functionality or operations of the database account.

5. After the upgrade is completed (status is `Upgraded`), select it to learn more about your next steps to finalize the process. If there's an issue processing your request, [contact support](https://azure.microsoft.com/support/create-ticket/).

6. Do one of the following:
    - If you upgraded from 3.2, go back to the `Overview` blade, and copy the new connection string to use in your application. The old connection string running 3.2 will not be interrupted. To ensure a consistent experience, all your applications must use the new endpoint.
    - If you upgraded from 3.6, your existing connection string will be upgraded to the version specified and should continue to be used.

## How to downgrade

You may also downgrade your account from 4.0 to 3.6 via the same steps in the preceding section, "How to Upgrade."

If you upgraded from 3.2 to (4.0 or 3.6) and wish to downgrade back to 3.2, simply switch back to using your previous (3.2) connection string: `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.documents.azure.com`, which remains active post-upgrade running version 3.2.

## **Recommended Documents**

- Learn more about the [supported and unsupported features of MongoDB version 4.0](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40).
- Learn more about the [supported and unsupported features of MongoDB version 3.6](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36).
- Learn more about [server-side retries](https://docs.microsoft.com/azure/cosmos-db/prevent-rate-limiting-errors).
