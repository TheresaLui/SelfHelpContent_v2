<properties
	pageTitle="Create Azure Cosmos DB resources using ARM template, PowerShell, Azure CLI or CSharp application"
	description="Troubleshoot CosmosDB PowerShell or Azure CLI related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="resource"
	supportTopicIds="32636824,32675641"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-admin-azurecli-powershell"
	displayOrder="21"
	category="Administration"
/>

# Creating and managing Azure Cosmos DB account and resources

You can create and manage all Azure Cosmos DB resources (across all APIs) from an ARM template, PowerShell or Azure CLI as well as dynamically change throughput (RU/s) on both database and container resources. You can also create and manage database and container resources from using any of the Cosmos DB SDK's as well as dynamically change throughput (RU/s).

## **Recommended Steps**

### Create an account, database and container using ARM templates and update RU/s

* [Manage Azure Cosmos DB SQL (Core) API resources using ARM Templates](https://docs.microsoft.com/azure/cosmos-db/manage-sql-with-resource-manager)
* [Azure Resource Manager templates for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/resource-manager-samples)

### Create an account, database and container using PowerShell and update RU/s

* [Manage Azure Cosmos DB SQL (Core) API resources using PowerShell](https://docs.microsoft.com/azure/cosmos-db/manage-with-powershell)
* [PowerShell samples for SQL (Core) API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-sql)
* [PowerShell samples for Cassandra API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-cassandra)
* [PowerShell samples for MongoDB API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-mongodb)
* [PowerShell samples for Gremlin API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-gremlin)
* [PowerShell samples for Table API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-table)

### Create an account, database and container using Azure CLI and update RU/s

* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)

### Create an account, database and container using .NET SDK and update RU/s

* [Database samples](https://docs.microsoft.com/azure/cosmos-db/sql-api-dotnet-samples#database-examples)
* [Container samples](https://docs.microsoft.com/azure/cosmos-db/sql-api-dotnet-samples#collection-examples)

## Known Issues

### Unable to create a collection with unique key from Azure CLI

The Azure CLI does not yet support commands to create unique keys with Azure Cosmos DB. However, support for unique key creation is in our roadmap. Use [.Net SDKs for SQL API](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) and [Mongo API for Mongo](https://docs.microsoft.com/azure/cosmos-db/unique-keys#mongodb-api-sample) to create unique keys per collection. Table API and Gremlin API do not support unique keys at the moment.

## **Recommended Documents**

* [Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
* [Managing Azure Cosmos account](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
* [Manage Azure Cosmos using PowerShell](https://docs.microsoft.com/azure/cosmos-db/manage-with-powershell)
* [Manage Azure Cosmos using Azure CLI](https://docs.microsoft.com/azure/cosmos-db/manage-with-cli)
