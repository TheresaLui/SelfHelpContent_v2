<properties
	pageTitle="CosmosDB Table API performance tips"
	description="CosmosDB Table API performance tips"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="66"
	selfHelpType="resource"
	supportTopicIds="32597548"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB - Table API

In order to achieve the best performance for Cosmos DB Table API, there are a few aspects you can configure: 

1. Use direct connection mode and TCP protocol whenever possible
2. Collocate clients in same Azure region for performance
3. Increase parallelism and connection count in the client
4. Use singleton Azure Cosmos DB Table API client for the lifetime of your application
5. Exclude unused paths from indexing for faster writes
5. Design for smaller documents for higher throughput

## **Recommended documents**
* [Table offerings](https://docs.microsoft.com/azure/cosmos-db/table-introduction)

* Note: OpenAsync is not available for Table API
