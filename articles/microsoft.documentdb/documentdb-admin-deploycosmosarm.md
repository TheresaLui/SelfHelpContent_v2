<properties
	pageTitle="Deploy Azure Cosmos DB using Azure Resource Manager template"
  description="Azure Cosmos DB via ARM Template"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="77"
	selfHelpType="resource"
	supportTopicIds="32597489"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Deploy Azure Cosmos DB using Azure Resource Manager template

You can create and manage Azure Cosmos DB accounts from an ARM template. The ARM template does not support creating database and collection.  However, you can use a C# console application or the Azure CLI to a create database and collection following the examples below.

### Managing resources with a C# console application

 1. [Create your database account in single region  using template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/)  or [create your database account in multi region using template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)
 

 2. [Create your database or collection using this Sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101)

### Managing resources using the Azure CLI

 1. [Create your account, database and collection using Azure CLI command](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)
* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
