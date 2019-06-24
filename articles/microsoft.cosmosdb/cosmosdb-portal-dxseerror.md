<properties
	pageTitle="Azure Cosmos DB error in data explorer"
	description="Error in Data Explorer"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="deborahc"
	ms.author="dech"
	selfHelpType="generic"
	supportTopicIds="32636780,32636790"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-portal-dxseerror"
/>

# I am getting an error when browsing data through Azure Cosmos DB Data Explorer

### Caching issues
To ensure you are using the latest version of the Data Explorer, clear your browser cache. Load the Data Explorer in Incognito or private browsing mode. If the issue continues to occur there, please contact us for support. 

### MongoDB API data format mismatch
The Data Explorer uses the native SDK based on the Cosmos DB Account API type to access the data from the Azure Cosmos DB. 

Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against a MongoDB API account will not generate any error. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.

### Query results not as expected
By default, the Data Explorer returns query results in pages, with up to 100 results per page. To view additional pages of results, select the **"Load more"** button under the results tab. You can adjust the maximum number of results per page in the Data Explorer **Settings** tab. 

## **Recommended Steps**

* If the issue is due to data format mismatch, use the native MongoDB SDKs to perform CRUD operations against your Azure Cosmos DB MongoDB API account
* Otherwise, load the Data Explorer in Incognito or private browsing mode. If the issue does not occur there, then clearing your cache in your original browsing session will resolve the issue. 

## **Recommended Documents**

* [Get started with Azure Cosmos DB MongoDB API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started)
