<properties
	pageTitle="CosmosDB performance tips - dot net"
	description="CosmosDB performance tips - dot net"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds="32597565"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB and .NET

In order to achieve the best performance for Cosmos DB using .NET clients, there are a few aspects you can configure: 
1. Use Direct Connection mode and TCP protocol whenever possible
2. Call OpenAsync() to avoid startup latency on first request
3. Collocate clients in same Azure region for performance
4. Increase parallelism and connection count in the client
5. Use singleton Azure Cosmos DB client for the lifetime of your application
6. Excluse unused paths from indexing for faster writes
7. Design for smaller documents for higher throughput

## **Recommended documents**
[Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips) provides detailed guidance on how to get the maximum performance for Cosmos DB using .NET clients 
