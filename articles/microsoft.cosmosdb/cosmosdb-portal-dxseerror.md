<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636780,32636790"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-portal-dxseerror"
/>

# I am getting an error when browsing data through Azure Cosmos DB Data Explorer
The Data Explorer uses the native SDK based on the Cosmos DB Account API type to access the data from the Azure Cosmos DB. Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against MongoDB API account would not generate any error. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.

## **Recommended Steps**
Using the native MongoDB SDKs to perform CRUD operations against Azure Cosmos DB MongoDB API account would help you to resolve this issue. You can review [Get started with Azure Cosmos DB MongoDB API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started) for building applications.
