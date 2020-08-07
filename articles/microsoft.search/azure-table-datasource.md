<properties
	pageTitle="Issue indexing an Azure Table data source"
	description="Issue indexing an Azure Table data source"
	service="microsoft.search"
	resource="searchservices"
	authors="luiscabrer"
	ms.author="luisca"
	selfHelpType="resource"
	displayOrder="4"	
	supportTopicIds="32681366"
	resourceTags=""
	productPesIds="15568"
	articleId="azure-table-datasource"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue indexing an Azure Table data source

## **Recommended Steps**

If you are having trouble indexing an Azure Table data source, you may want to ensure that:

1. Your data is populated in the database
1. The data source properties (name, type, credentials, container) are set correctly as described [here](https://docs.microsoft.com/azure/search/search-howto-indexing-azure-tables)
1. The key value does not contain invalid characters. You can deal with invalid characters by using the [base64Encode field mapping function](https://docs.microsoft.com/azure/search/search-indexer-field-mappings#base64EncodeFunction). If you do this, remember to also use URL-safe Base64 encoding when passing document keys in API calls such as Lookup.
	
## **Recommended Documents**

* [Index Azure Table storage with Azure Search](https://docs.microsoft.com/azure/search/search-howto-indexing-azure-tables) 
