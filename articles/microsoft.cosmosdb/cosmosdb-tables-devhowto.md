<properties
	pageTitle="How to get started with Azure Cosmos DB Tables" 
	description="How to get started with Azure Cosmos DB Tables"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636750"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"	
	articleId="cosmosdb-tables-devhowto"
	displayOrder="300"
	category="Azure Table"
/>

# How to develop applications with Azure Cosmos DB Table API

Applications written for Azure Table storage can migrate to Azure Cosmos DB by using the Table API.

To get started:

* Replace your connection string to connect to an Azure Cosmos DB account created with the Table API.
* Make sure to use the latest version of your Azure Table Storage driver or SDK; if your application is running on .NET, we recommend to use the [Azure Cosmos DB Table .NET Standard SDK](https://docs.microsoft.com/azure/cosmos-db/table-sdk-dotnet-standard).
* Get familiar with Azure Cosmos DB's provisioned throughput model and evaluate how many [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units) your application might need.

Then, learn about the premium capabilities you can leverage:

* Automatic secondary indexing: all columns get automatically indexed by default
* [Global distribution](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally): tables can be replicated to any Azure datacenter to ensure low latency and high availability

## **Recommended Documents**

* [Introduction to Azure Cosmos DB: Table API](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
* [Azure Storage Table Design Guide: Designing Scalable and Performant Tables](https://docs.microsoft.com/azure/cosmos-db/table-storage-design-guide)
