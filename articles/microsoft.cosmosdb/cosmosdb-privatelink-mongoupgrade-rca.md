<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade recommendation for Private Link accounts RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account using Private Link recommended to upgrade to v4.0"
    infoBubbleText="The customer's account is recommended upgrade to Azure Cosmos DB API for MongoDB v4.0 as it uses Private Link"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-privatelink-mongoupgrade-rca"
    diagnosticScenario="CosmosDBPrivateLinkMongoUpgradeInsight"
    selfHelpType="rca"
    supportTopicIds="32738664, 32738665"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Upgrade MongoDB API version to use Azure Private Link

## Action Required

As an Azure Private Link customer, your database account, <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> is recommended to be updated to the latest version of Azure Cosmos DB's API for MongoDB

<!--issueDescription-->
Version 3.2 of Azure Cosmos DB's API for MongoDB is not compatible with Azure Private Link. Upgrading to the latest version of the service will enable compatibility with Private Link and provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

## Upgrading to 4.0 or 3.6

### Benefits of upgrading to version 4.0

The following are the new features included in version 4.0:
- Support for multi-document transactions within unsharded collections.
- New aggregation operators
- Enhanced scan performance
- Faster, more efficient storage

### Benefits of upgrading to version 3.6

The following are the new features included in version 3.6:
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
- Per request timeout is set to 60 seconds.
- MongoDB collections created on the new wire protocol version will only have the `_id` property indexed by default.

### Action required when upgrading from 3.2

When upgrading from 3.2, the database account endpoint suffix will be updated to the following format:

```
<your_database_account_name>.mongo.cosmos.azure.com
```

If you are upgrading from version 3.2, you will need to replace the existing endpoint in your applications and drivers that connect with this database account. **Only connections that are using the new endpoint will have access to the features in the new API version**. The previous 3.2 endpoint should have the suffix `.documents.azure.com`.

>[!Note]
> This endpoint might have slight differences if your account was created in a Sovereign, Government or Restricted Azure Cloud.

## How to upgrade

1. Go to the Azure portal and navigate to your Azure Cosmos DB API for MongoDB account overview blade. Verify your current server version is what you expect.

2. From the options on the left, select the `Features` blade. This will reveal the Account level features that are available for your database account.

3. Click on the `Upgrade Mongo server version` row. If you don't see this option, your account might not be eligible for this upgrade. Please file [a support ticket](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) if that is the case.


4. Review the information displayed about the upgrade. Click on `Enable` as soon as you are ready to start the process.

5. After starting the process, the `Features` menu will show the status of the upgrade. The status will go from `Pending`, to `In Progress`, to `Upgraded`. This process will not affect the existing functionality or operations of the database account.


6. Once the upgrade is completed, the status will show as `Upgraded`. Click on it to learn more about the next steps and actions you need to take to finalize the process. Please [contact support](https://azure.microsoft.com/en-us/support/create-ticket/) if there was an issue processing your request.

7. 
    1. If you upgraded from 3.2, go back to the `Overview` blade, and copy the new connection string to use in your application. The old connection string running 3.2 will not be interrupted. To ensure a consistent experience, all your applications must use the new endpoint.
    2. If you upgraded from 3.6, your existing connection string will be upgraded to the version specified and should continue to be used.



## How to downgrade
You may also downgrade your account from 4.0 to 3.6 via the same steps in the 'How to Upgrade' section. 

If you upgraded from 3.2 to (4.0 or 3.6) and wish to downgrade back to 3.2, you can simply switch back to using your previous (3.2) connection string with the host `accountname.documents.azure.com` which remains active post-upgrade running version 3.2.


## **Recommended Documents**

- Learn about the supported and unsupported [features of MongoDB version 4.0](mongodb-feature-support-40.md).
- Learn about the supported and unsupported [features of MongoDB version 3.6](mongodb-feature-support-36.md).
- For further information check [Mongo 3.6 version features](https://devblogs.microsoft.com/cosmosdb/azure-cosmos-dbs-api-for-mongodb-now-supports-server-version-3-6/)
- [Azure Private Link](https://docs.microsoft.com/azure/private-link/private-link-overview)
- [Azure Private Link for Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints)