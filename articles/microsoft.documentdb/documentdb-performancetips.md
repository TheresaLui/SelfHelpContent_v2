<properties
	pageTitle="CosmosDB performance tips"
	description="CosmosDB performance tips"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32597551,32597550,32597548,32597549"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB

In order to achieve the best performance for Cosmos DB, there are a few aspects you can configure: 
1. Use Direct Connection mode and TCP protocol whenever possible
2. Call OpenAsync() to avoid startup latency on first request (for .NET clients)
3. Collocate clients in same Azure region for performance
4. Increase parallelism and connection count in the client
5. Use singleton Azure Cosmos DB client for the lifetime of your application
6. Excluse unused paths from indexing for faster writes
7. Design for smaller documents for higher throughput

## **Recommended documents**
[Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
[Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
[Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java) 
