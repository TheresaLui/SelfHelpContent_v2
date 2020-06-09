<properties
    pageTitle="Azure Cosmos DB API for MongoDB upgrade recommendation for Private Link accounts RCA"
    description="RCA - Azure Cosmos DB API for MongoDB v3.2 account using Private Link recommended to upgrade to v3.6"
    infoBubbleText="The customer's account is recommended upgrade to Azure Cosmos DB API for MongoDB v3.6 as it uses Private Link"
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

# Upgrade to MongoDB API engine version 3.6 to use Azure Private Link

## As an Azure Private Link customer, your database account, <!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName--> is recommended to be updated to the latest version of Azure Cosmos DB's API for MongoDB

<!--issueDescription-->
Version 3.2 of Azure Cosmos DB's API for MongoDB is not compatible with Azure Private Link. Upgrading to the latest version of the service will enable compatibility with Private Link and provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

<!--/issueDescription-->

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
   - Per request timeout is going to be 60 seconds

3. Action required

   Please file a support ticket to get your Mongo version updated.

## **Recommended Documents**

- [Azure Cosmos DB's API for MongoDB (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
- [Azure Private Link](https://docs.microsoft.com/azure/private-link/private-link-overview)
- [Azure Private Link for Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints)
