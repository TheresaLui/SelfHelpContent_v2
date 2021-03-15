<properties
	pageTitle="CosmosDB enable change feed for MongoDB API"
	description="CosmosDB enable change feed for MongoDB API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jasontho"
	ms.author="jasontho"
	selfHelpType="generic"
	supportTopicIds="32747699"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongo-enablechangefeed"
	displayOrder="227"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Enable Change Feed for Azure Cosmos DB MongoDB API

## **Recommended Steps**

* Change Feed is already enabled when using read-only keys. To consume the change feed, connect using a read-only key.
* For accounts on server version 3.6 or above, consider using [Change Streams](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-change-streams) instead of Change Feed.
