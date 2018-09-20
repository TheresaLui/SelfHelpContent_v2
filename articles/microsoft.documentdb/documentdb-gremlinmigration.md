<properties
	pageTitle="Gremlin Migration"
	description="Gremlin Development"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="26"
	selfHelpType="resource"
	supportTopicIds="32597507"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Gremlin - Importing data

## **Recommended Steps**

### **Graph BulkExecutor API**
Use Azure Cosmos DB's BulkExecutor library to import and update graph objects into an Azure Cosmos DB Gremlin API container. You can use this library to create Vertex and Edge objects programmatically to then insert multiple of them per network request.
You can configure the batch size via configuration options in the library to trade off database and local memory resource usage.

## **Recommended Documents**
* [Using the BulkExecutor API for Gremlin](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-graph-dotnet)
* [Graph BulkExecutor API reference](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmosdb.bulkexecutor.graph?view=azure-dotnet)
