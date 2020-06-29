<properties
	pageTitle="Portal import data wizard not suggesting the index schema"
	description="Portal import data wizard not suggesting the index schema"
	service="microsoft.search"
	resource="searchservices"
	authors="vkurpad"
	ms.author="vikurpad"
	selfHelpType="resource"
	displayOrder="8"	
	supportTopicIds="32681349"
	resourceTags=""
	productPesIds="15568"
	articleId="search-index-schema"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue with index schema in the import data wizard

## **Recommended Steps**

If you are having trouble with the index schema being suggested by the import data wizard, you may want to ensure that:

1. Your data source definition is valid, the wizard is able to read a file/record from the data source 
1. Ensure the first file/record matches your anticipated schema
1. Set your [parsing mode](https://docs.microsoft.com/azure/search/search-howto-index-json-blobs#parsing-modes) to use appropriate document cracker
	
## **Recommended Documents**

* [How to index JSON blobs using Azure Search Blob indexer](https://docs.microsoft.com/azure/search/search-howto-index-json-blobs) 
