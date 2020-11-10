<properties
    pageTitle="Metadata operations RCA"
    description="RCA - High number of metadata operations on collection"
    infoBubbleText="Found information related to Machine Key Status. See details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="bharathsreenivas"
    ms.author="bharathb"
    articleId="cosmosdb-metadataoperations-rca"
    diagnosticScenario="CosmosDBMetadataInsight"
    selfHelpType="rca"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# High number of metadata operations on collection

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We found a high number of metadata operations on your account.
<!--/issueDescription-->
In Cosmos DB, data is distributed across partitions. This includes metadata about your databases/collections. Metadata for Cosmos DB has a system-reserved request unit (RU) limit. You can avoid rate limiting from metadata operations by following these patterns.

## **Recommended Steps**

### Use static Cosmos DB client instances

Upon initialization of the *DocumentClient* constructor, the Cosmos DB SDK fetches metadata about the account including consistency level, databases, collections, partitions, and offers. This initialization may consume a high number of RUs, and should be performed infrequently. Use a single DocumentClient instance and use it for the lifetime of your application.

### Cache the names of databases/collections

Retrieve the names of your databases and collections from configuration or cache them on start. Calls like *ReadDatabaseAsync*/*ReadDocumentCollectionAsync* or *CreateDatabaseQuery*/*CreateDocumentCollectionQuery* will result in calls to the service, and will consume RUs. They should be performed infrequently.

## **Recommended Documents**

For other tips on performance and SDK best practices, please see [.NET tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips) and [Java tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java).
