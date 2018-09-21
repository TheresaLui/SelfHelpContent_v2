<properties
	pageTitle="Deploy Cosmos DB from Azure CLI & PowerShell"
	description="Deploy Cosmos DB from Azure CLI & PowerShell"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="77"
	selfHelpType="resource"
	supportTopicIds="32597494"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"/>

# Unable to create collection with unique key from CLI

Currently Azure Cosmos DB CLI does not support creating unique keys.  Support for unique key creation in Azure Cosmos DB CLI is in our roadmap. Use [Cosmos DB SDKs/Various APIs](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) to create unique keys per collection.



## Could not find Cmdlets to create Cosmos DB collection in PowerShell

The Azure Cosmos DB PowerShell does not yet support cmdlets to manage the runtime resource such as database, collection/tables/graphs, users, permissions, documents/items/nodes/edges/triggers/stored procedure/user defined function and attachments

You can use the below approaches to manage the runtime resources.

### Using the C# console application

* [Use PowerShell to create the account](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)
* [Use Sample C# code to create database and collection](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)

### Using the Azure CLI 

* [Use the Azure CLI command to create Database and Collection](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

## **Recommended documents**

* [Unique keys in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/unique-keys)
