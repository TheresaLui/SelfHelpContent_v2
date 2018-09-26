<properties
	pageTitle="CosmosDB performance tips for Gremlin API"
	description="CosmosDB performance tips for Gremlin API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="30"
	selfHelpType="resource"
	supportTopicIds="32597549"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB Gremlin API

In order to achieve the best performance for the Gremlin API, there are a few aspects you can configure: 

1. Collocate clients in same Azure region for performance.
2. Increase parallelism on the client whenever possible.
3. Use singleton Azure Cosmos DB client for the lifetime of your application.
4. Design for accessing smaller vertices for higher throughput.
5. Gremlin queries consume RUs based on the number of edges/vertices that are read and written by them. Consider breaking up complex Gremlin queries into smaller sub-queries in sequence to identify where the bottleneck may be.
6. For queries that involve a multi-edge hop, RUs consumed will be higher since the vertices might be in different partitions. Consider breaking up such queries, if possible. 

## **Recommended documents**
Some of the [performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips) described are useful to keep in mind while designing an application which is using the Gremlin API

