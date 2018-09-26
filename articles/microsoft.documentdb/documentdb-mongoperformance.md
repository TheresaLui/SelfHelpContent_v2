<properties
	pageTitle="CosmosDB performance tips for MongoDB API"
	description="CosmosDB performance tips for MongoDB API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="28"
	selfHelpType="resource"
	supportTopicIds="32597550"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB MongoDB API

In order to achieve the best performance for Azure Cosmos DB MongoDB API, there are a few aspects you can configure: 

1. Collocate clients in same Azure region for performance.
2. Increase parallelism on the client whenever possible.
3. Use singleton Azure Cosmos DB client for the lifetime of your application.
4. Excluse unused paths from indexing for faster writes.
5. Design for smaller documents for higher throughput.

## **Recommended documents**
Some of the [performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips) described are useful to keep in mind while designing an application which is using the MongoDB API

