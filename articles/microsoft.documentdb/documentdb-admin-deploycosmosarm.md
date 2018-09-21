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

You can create and manage Azure Cosmos DB Accounts from Azure Resource Manager Template. To automate Databases, Collections, and other resources, please use one of the supported SDKs based on your chosen API kind.

Please refer the below sample template for reference.

[Create an Azure Cosmos DB API account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/)

[Create a Multi-Region Azure Cosmos DB Database Account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)  

You can use the below approaches to manage runtime resources (database/collection)

### Using the C# Console Application

* Use the [template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/) to create the account

* Use the [Sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101) to create database and collection

### Using the Azure CLI

* Use the above [template](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/) to create the account or use the [Azure CLI](https://docs.microsoft.com/azure/cosmos-db/cli-samples) to create the account

* Use the [Azure CLI command](https://docs.microsoft.com/azure/cosmos-db/cli-samples) to create database and collection.  

## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)
* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
