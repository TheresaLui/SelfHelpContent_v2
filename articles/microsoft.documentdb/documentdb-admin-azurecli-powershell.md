<properties
	pageTitle="Deploy Azure Cosmos DB from Azure CLI & PowerShell"
	description="Deploy Azure Cosmos DB from Azure CLI & PowerShell"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="77"
	selfHelpType="resource"
	supportTopicIds="32597494"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"/>

# Unable to create a collection with unique key from Azure CLI

The Azure CLI does not yet support commands to create unique keys with Azure Cosmos DB. However, support for unique key creation is in our roadmap. Use [.Net SDKs for SQL API](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) and [Mongo API for Mongo](https://docs.microsoft.com/azure/cosmos-db/unique-keys#mongodb-api-sample) to create unique keys per collection.  The Table API and Gremlin API do not support unique keys at the moment.



## Could not find cmdlets to create Azure Cosmos DB collection in PowerShell

The Azure PowerShell does not yet support cmdlets to manage Azure Cosmos DB runtime resource such as database, collection/tables/graphs, users, permissions, documents/items/nodes/edges/triggers/stored procedure/user defined function and attachments.

You can use the following approaches to manage the runtime resources.

### Using the C# console application

* [Use PowerShell to create the account](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)
* [Use Sample C# code to create database and collection](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)

### Using the Azure CLI 

* [Use the Azure CLI command to create database and collection](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

## **Recommended documents**

* [Unique keys in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/unique-keys)
