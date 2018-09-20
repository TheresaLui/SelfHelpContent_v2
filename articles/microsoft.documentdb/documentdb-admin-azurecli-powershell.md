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

# Unable to create Collection with Unique Key from CLI

Use [Cosmos DB SDKs](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) to create Unique Keys per Collection.  Support for Unique Key definition in the Azure CLI is in our Roadmap.



# Could not find Cmd-lets to create Cosmos DB Collection in PowerShell

The Azure Cosmos DB PowerShell does not have Cmd-lets to manage the runtime resource such as Database, Collection/Tables/graphs, Users, Permissions, documents/items/nodes/edges and attachments

You can use the below approaches to manage the runtime resources.

### Using the C# Console Application

* [Use PowerShell to create the account](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)
* [Use Sample C# code to create Database and Collection](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)

### Using the Azure CLI 

* [Use the Azure CLI command to create Database and Collection](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

### **Recommended documents**
* [Unique keys in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/unique-keys)
