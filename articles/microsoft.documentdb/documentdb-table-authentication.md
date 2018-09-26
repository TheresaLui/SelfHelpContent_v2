<properties
	pageTitle="Azure CosmosDB table authentication"
	description="Authentication"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	displayOrder="69"
	selfHelpType="resource"
	supportTopicIds="32597493"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# I am getting authentication failure to my Azure Cosmos DB table collection

## **Recommended Steps**

To resolve this issues, try the following methods

* Verify the correct secret key is used by the application
* Validate the connection string from the Azure Portal - Cosmos DB Connection string tab and compare with string in the application.
* Carefully review the secret key and remove any spaces at the start or at the end of the string.




## **Recommended documents**

* [Securing access to Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data)
* [Access Control on Azure Cosmos DB Resources](https://docs.microsoft.com/rest/api/cosmos-db/access-control-on-cosmosdb-resources)
* [Azure Cosmos DB database security](https://docs.microsoft.com/azure/cosmos-db/database-security)
