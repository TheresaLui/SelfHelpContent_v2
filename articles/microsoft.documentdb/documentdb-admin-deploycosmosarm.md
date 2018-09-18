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
	productPesIds=""
	cloudEnvironments="public"
/>
# Deploy Cosmos DB using ARM Template

The Azure Cosmos DB resources are classified namely  Account, Database,  Collection and so on. Please review [Cosmos DB Resource model](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources) for complete list. The Database, Collection/Tables/graphs, Users, Permissions, documents/items/nodes/edges, attachments  resources types are all runtime resources. You manage (CRUD/query) these resources using SDKs and REST APIs. For instance, you can use any of the MongoDB client drivers to  program against databases, collections, documents etc. Likewise, you can use a Gremlin clients to query/CRUD the graph, nodes and edges and so on. All of the “runtime resources”are meant to  be used by the developers directly inside their applications.

In the Azure Cosmos DB resource hierarchy, you have a database account, which contains databases, which contains containers (collections). Only the database account is an ARM (control plane) resource, and databases/collections/other resources are run-time/data plane resources.

Please refer the below sample template for references.

[Create an Azure Cosmos DB API account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-arm-template/)

[Create a Multi-Region Azure Cosmos DB Database Account](https://azure.microsoft.com/resources/templates/101-cosmosdb-create-multi-region-account/)  

You can use the below approaches to manage runtime resources (database/collection)

Using the C# Console Application
* Use the above template to create the account
* Use the [Sample C# code](https://github.com/Azure/azure-cosmosdb-dotnet/blob/89670bc8aefd9bdd932db7f9b6d2fcb9b6acf35e/samples/code-samples/CollectionManagement/Program.cs#L101) to create database and collection

Using the Azure CLI
* Use the above template to create the account or use the Azure CLI to create the account
* Use the [Azure cli command](https://docs.microsoft.com/azure/cosmos-db/cli-samples) create database and collection.  

## **Recommended documents**

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
