<properties
	pageTitle="Issue creating an indexer"
	description="Issue creating an indexer"
	service="microsoft.search"
	resource="searchservices"
	authors="MarkHeff"
	ms.author="maheff"
	selfHelpType="resource"
	supportTopicIds="32681357"
	displayOrder="36"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="indexer-create-issue"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating an indexer

## **Recommended Steps**

If you are having trouble creating an indexer, consider the following:

1. If you've received an error related to the data source connection make sure that the connection string is correct.
1. Confirm that in the indexer definition the data source name, target index name, and skillset name, if you have a skillset, are correct.
1. When specifying field mappings ensure that the source and target fields are correct.

## **Recommended Documents**

* [Indexers in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-indexer-overview)
* [Indexer operations (REST API)](https://docs.microsoft.com/rest/api/searchservice/Indexer-operations)
* [IIndexersOperations Interface (.NET SDK)](https://docs.microsoft.com/dotnet/api/microsoft.azure.search.iindexersoperations?view=azure-dotnet)