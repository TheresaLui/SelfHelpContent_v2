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
	productPesIds=""
	cloudEnvironments="public"/>

# Unable to create collection with Unique Key from CLI

The Azure Cli does not have option to create collection with Unique Key yet.  We would be enchacing the cli command to include the Unique Key option in coming months.  However, for now you can use the Cosmos DB SDKs to create the collection with Unique Key. Please refer [Collection Creation Sample](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample)


## Could not find command-lets to create cosmos db collection in Powerhshell

The Azure Cosmos DB Powershell does not have command-lets to manage the runtime resource such as Database, Collection/Tables/graphs, Users, Permissions, documents/items/nodes/edges and attachments

You can use the below approaches to manage the runtime resources.

## Using the C# Console Application

* [Use Powershell to create the account](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)
* [Use Sample C# code to create database and collection](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)

## Using the Azure CLI 

* [Use the Azure cli command create database and collection](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

## **Recommended documents**
* [Azure Cosmos Cli Samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

* [Unique keys in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/unique-keys)
