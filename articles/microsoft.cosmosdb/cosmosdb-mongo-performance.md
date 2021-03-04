<properties
	pageTitle="CosmosDB performance tips for MongoDB API"
	description="CosmosDB performance tips for MongoDB API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="generic"
	supportTopicIds="32636819"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongo-performance"
	displayOrder="226"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Performance tips for Azure Cosmos DB MongoDB API

## **Recommended Steps**

To achieve optimal performance for Azure Cosmos DB MongoDB API, there are a few aspects you can configure:
* Collocate clients in same Azure region
* Increase parallelism on the client, whenever possible
* Use singleton Azure Cosmos DB client for the lifetime of your application
* Exclude unused paths from indexing for faster writes
* Design for smaller documents for higher throughput


### **Deleting large amounts of data**
If you're wanting to delete large amounts of data without impacting RU:
* Consider using TTL (Based on Timestamp). See [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live).
* Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This helps you to slowly delete without impacting your production application.


## **Recommended Documents**  
[Azure Cosmos DB's API for MongoDB (4.0 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40)
<br>The supported operators and any limitations or exceptions are listed in this article for API version 4.0. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.

## **FAQs on Server Side Retries(SSR)**  

#### Are there any best practices to consider when enabling SSR? 
If your application is working without many 16500 errors without SSR, it should work great with SSR. If you do see timeout errors, the body of the exception will tell you if it was because of SSR, and it will be an indication that RUs were exceeded for over a minute. SSR works best when combined with autoscale.

#### How long (and how many times) will the server retry?
Server will retry unlimited times up to request timeout of 60 seconds. 

#### Will SSR have an impact on the consistency level? 
No 

#### Does SSR effect all requests? So will a read request wait in line and slow down the application?
It affects all requests. Application is only slowed if requests are experiencing rate limiting, and will be slowed instead of fail. 

#### Can we monitor the effects of SSR? For example queuelength, responsetime
There is no strict queue. best way to monitor effect is look at ~P99 times in Azure Diagnostics. 
