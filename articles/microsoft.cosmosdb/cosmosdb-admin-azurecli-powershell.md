<properties
	pageTitle="Create Azure Cosmos DB account using ARM template or PowerShell and manage resources using Azure CLI or C# application"
	description="Create Azure Cosmos DB account using ARM template or PowerShell and manage resources using Azure CLI or C# application"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636824"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-admin-azurecli-powershell"
/>

# Creating Azure Cosmos DB account and managing resources

You can create and manage Azure Cosmos DB accounts from an ARM template or PowerShell but creating databases and collections using ARM templates or PowerShell is not yet supported.  However, you can use a C# console application or Azure CLI to create databases and collections following the examples below.

## Creating an account using ARM template

* Using the appropriate ARM template, create your database account in a [single region](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-account/)  or [multiple regions](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)
 

## Creating an account using PowerShell

* [Create your account using PowerShell](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)


## Managing the resources with a C# console application

* [Create your database and collection using this sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)


## Managing the resources using the Azure CLI commands

* [Create your database and collection using these Azure CLI commands](https://docs.microsoft.com/azure/cosmos-db/cli-samples)


### Known Issue : Unable to create a collection with unique key from Azure CLI

The Azure CLI does not yet support commands to create unique keys with Azure Cosmos DB. However, support for unique key creation is in our roadmap. Use [.Net SDKs for SQL API](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) and [Mongo API for Mongo](https://docs.microsoft.com/azure/cosmos-db/unique-keys#mongodb-api-sample) to create unique keys per collection.  The Table API and Gremlin API do not support unique keys at the moment.


### Known Issue : Could not find cmdlets to create Azure Cosmos DB collection in PowerShell

The Azure PowerShell does not yet support cmdlets to manage Azure Cosmos DB runtime resource such as databases, collections, tables, graphs, users, permissions, documents, items, nodes, edges, triggers, stored procedures, user defined functions and attachments.

However, you can use a C# console application or the Azure CLI to manage runtime resources following the examples below.


## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
