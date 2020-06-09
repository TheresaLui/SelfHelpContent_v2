<properties
	pageTitle="Create Azure Cosmos DB resources using ARM template, PowerShell, Azure CLI or CSharp application"
	description="Troubleshoot Cosmos DB PowerShell or Azure CLI related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636824,32675641"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-admin-azurecli-powershell"
	displayOrder="21"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Creating and managing Azure Cosmos DB account and resources

You can create and manage all Azure Cosmos DB resources (across all APIs) from an ARM template, PowerShell or Azure CLI as well as dynamically change throughput (RU/s) on both database and container resources. You can also create and manage database and container resources from using any of the Cosmos DB SDK's as well as dynamically change throughput (RU/s).

## **Recommended Steps**


### **Questions About the apiVersion specified in the Cosmos DB ARM template**  

**Question:** I am creating Cosmos DB with ARM template. The ARM template specified at the time of creation is manually followed by *apiVersion: 2015-04-08*, but when you download and check the template after creation, It had become a new date *example: 2019-08-01*. Is it a specification?
- Yes, API version is not a resource-related version of Cosmos DB account, but is the version of the API used when deploying. When you download a template from the Azure portal, it is output by default with the latest API version date *example: 2019-08-01*.  


**Question:** If you specify a date *example: 2019-08-01*, are there any changes to the configuration and settings of the Cosmos DB database account created by the difference in API versions?
- If you specify *example: 2019-08-01*, there is no change in the configuration and settings of the Cosmos DB database account created by the difference in API version. However, if the API version is *2019-08-01* and *2015-04-08*, the format of the database and the JSON file used when creating the container is different. When creating a database or container using a different API version please refer to the documentation [2019-08-01](https://docs.microsoft.com/azure/templates/microsoft.documentdb/2019-08-01/databaseaccounts)  and [2015-04-08](https://docs.microsoft.com/azure/templates/microsoft.documentdb/2015-04-08/databaseaccounts).  


### **Feature update not available using ARM template**  
**Symptom:** Your ARM template works when initially provisioning a Cosmos DB with the features enabled, but it does not work when trying to enable the features after the cosmos DB has been provisioned for the first time.  
**Solution:** Current behavior is feature updates are not available thru ARM template. Please use the portal to manually set it or create an account with the preview feature enabled.

### **Unable to create a collection with unique key from Azure CLI**  
The Azure CLI does not yet support commands to create unique keys with Azure Cosmos DB. However, support for unique key creation is in our roadmap. Use [.Net SDKs for SQL API](https://docs.microsoft.com/azure/cosmos-db/unique-keys#sql-api-sample) and [Mongo API for Mongo](https://docs.microsoft.com/azure/cosmos-db/unique-keys#mongodb-api-sample) to create unique keys per collection. Table API and Gremlin API do not support unique keys at the moment.


## **Recommended Documents**  

[Managing Azure Cosmos account](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.  

[Azure Cosmos DB hierarchical resource model and core concepts](https://docs.microsoft.com/azure/cosmos-db/sql-api-resources)
<br>After you create an Azure Cosmos DB account under your Azure subscription, you can manage data in your account by creating databases, containers, and items. This article describes each of these entities.  

[Manage Azure Cosmos using PowerShell](https://docs.microsoft.com/azure/cosmos-db/manage-with-powershell)
<br>This guide describes how to use PowerShell to script and automate management of Azure Cosmos DB resources, including account, database, container, and throughput. Management of Azure Cosmos DB is handled through the AzResource cmdlet directly to the Azure Cosmos DB resource provider.   

[Manage Azure Cosmos using Azure CLI](https://docs.microsoft.com/azure/cosmos-db/manage-with-cli)
<br>The following guide describes common commands to automate management of your Azure Cosmos DB accounts, databases and containers using Azure CLI. Reference pages for all Azure Cosmos DB CLI commands are available in the Azure CLI Reference.  

Examples for Create an account, database and container using ARM templates and update RU/s
* [Manage Azure Cosmos DB SQL (Core) API resources using ARM Templates](https://docs.microsoft.com/azure/cosmos-db/manage-sql-with-resource-manager)
* [Azure Resource Manager templates for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/resource-manager-samples)
* [Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)


Powershell samples for Create an account, database and container using PowerShell and update RU/s
* [PowerShell samples for SQL (Core) API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-sql)
* [PowerShell samples for Cassandra API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-cassandra)
* [PowerShell samples for MongoDB API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-mongodb)
* [PowerShell samples for Gremlin API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-gremlin)
* [PowerShell samples for Table API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-table)  


Create an account, database and container using .NET SDK and update RU/s
* [Database samples](https://docs.microsoft.com/azure/cosmos-db/sql-api-dotnet-samples#database-examples)
* [Container samples](https://docs.microsoft.com/azure/cosmos-db/sql-api-dotnet-samples#collection-examples)

