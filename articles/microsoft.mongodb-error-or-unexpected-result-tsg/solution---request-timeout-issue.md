<properties
	pageTitle="Request timeout issue"
	description="Request timeout issue"
	service="Microsoft.DocumentDB"
	resource="databaseAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7b5c3e2e-64f8-4fcb-a972-9d8daeff5e96"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Request timeout issue

<!--issueDescription-->

While executing a query using the Mongo API for Cosmos DB, the request might timeout when there is large amount of data to be processed. Increasing the collection throughput would help mitigate this issue. You can also evaluate if the queries can be optimized further by making effective use of the index.

If you are wanting to delete large amounts of data without impacting RU:
1. Consider using TTL (Based on Timestamp): [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-time-to-live), this will help decrease the number of documents gradually having just a very small impact on the RUs consumed, therefore, you will not get a timeout.
2. Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This would help you to slowly delete without impacting your production application.

<!--/issueDescription-->

## Recommended Documents

1. [Cosmos DB TTL](https://docs.microsoft.com/azure/cosmos-db/time-to-live)

