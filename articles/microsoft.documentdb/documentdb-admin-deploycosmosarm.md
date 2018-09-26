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

You can create and manage Azure Cosmos DB accounts from ARM template. Please use the following sample template for creating Cosmos DB account.

[Create an Azure Cosmos DB API account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/)

[Create a multi-region Azure Cosmos DB database account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)  

But the ARM template does not support creating database and collection.  However, you can use any of the approaches given below to create database and collection.

### Using the C# console application

 1. Use the [template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/) to create the account.

 2. Use the [Sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101) to create the database and collection.

### Using the Azure CLI

 1. Use the [Azure CLI command](https://docs.microsoft.com/azure/cosmos-db/cli-samples) to create the account, database and collection.  

## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)
* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
