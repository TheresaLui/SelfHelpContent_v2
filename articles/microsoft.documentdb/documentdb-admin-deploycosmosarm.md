<properties
	pageTitle="Deploy Cosmos DB using ARM Template"
  description="Cosmos DB via ARM Template"
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
# Deploy Cosmos DB using ARM Template

You can create and manage Azure Cosmos DB accounts from Azure Resource Manager Template. But the Azure Resource Manager Template does not support creating database and collection.  However, you can use any of the approaches given below to create database and collection.


Please use the below sample template for creating Cosmos DB account.

[Create an Azure Cosmos DB API account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/)

[Create a multi-region Azure Cosmos DB database account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)  

You can use any of one of the below given approaches to create database or collection.

### Using the C# console application

 1. Use the [template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/) to create the account.

 2. Use the [Sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101) to create database and collection.

### Using the Azure CLI

 1. Use the [Azure CLI command](https://docs.microsoft.com/azure/cosmos-db/cli-samples) to create account, database and collection.  

## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)
* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
