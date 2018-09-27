<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="91"
	selfHelpType="resource"
	supportTopicIds="32597505,32597510,32597517,32597518"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# I am getting error when access Azure Cosmos data explorer

## **Recommended Steps**

The data explorer uses the respective SDK i.e. SQL API or Mongo API to access the data from the Azure Cosmos DB.  Using a Azure Cosmos DB - SQL API SDK to perform CRUD operation against Mongo API account 
would not generate any error.  However, this would make the data explorer to fail when reading the data due to structure mismatch.

Please use the Mongo SDKs to perform CRUD operation against Azure Cosmos DB Mongo API account.

## **Recommended documents**

* [Get started with Azure Cosmos DB Mongo API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started)
