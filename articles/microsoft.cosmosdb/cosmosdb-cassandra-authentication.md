<properties
	pageTitle="Azure CosmosDB Cassandra authentication"
	description="Authentication"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636769"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-cassandra-authentication"
/>

# Authentication failure error when connecting to Azure Cosmos DB Cassandra collection

## **Recommended Steps**

To resolve this issue, try the following methods:

* Validate that the connection string specified in your application matches with the Azure Cosmos DB connection string retrieved from the Connection string tab of the Azure Portal.
* Review the secret key and remove any spaces at the start or at the end of the string.
* Ensure that SSL is enabled in the connection options.



## **Recommended documents**

* [Securing access to Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data)
