<properties
	pageTitle="CosmosDB performance tips for MongoDB API"
	description="CosmosDB performance tips for MongoDB API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="resource"
	supportTopicIds="32636819"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-mongo-performance"
	displayOrder="226"
	category="MongoDB"
/>

# Performance tips for Azure Cosmos DB MongoDB API

## **Recommended Steps**

In order to achieve the best performance for Azure Cosmos DB MongoDB API, there are a few aspects you can configure: 

1. Collocate clients in same Azure region for performance.
2. Increase parallelism on the client whenever possible.
3. Use singleton Azure Cosmos DB client for the lifetime of your application.
4. Exclude unused paths from indexing for faster writes.
5. Design for smaller documents for higher throughput.

## **Recommended Documents**  
[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.6 by default for new accounts. The supported operators and any limitations or exceptions are listed in this articl. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips) 
<br>This article describes how you can improve your database performance.

