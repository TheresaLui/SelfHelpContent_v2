<properties
	pageTitle="Issue with indexer field mapping"
	description="Issue with indexer field mapping"
	service="microsoft.search"
	resource="searchservices"
	authors="vkurpad"
	ms.author="vikurpad"
	selfHelpType="resource"
	displayOrder="13"	
	supportTopicIds="32681378"
	resourceTags=""
	productPesIds="15568"
	articleId="indexer-field-mapping"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue with indexer field mapping

## **Recommended Steps**

If you are having trouble with an indexer field mapping, you may want to ensure that:

1. Your index field names and data source field names match 
1. The data type of the index field matches the data type of the mapped field
1. You are using a [mapping function to transform a field's contents](https://docs.microsoft.com/azure/search/search-indexer-field-mappings) if your field has special characters
1. If you are mapping an enriched field using Cognitive Search, see [output field mappings](https://docs.microsoft.com/azure/search/cognitive-search-output-field-mapping)
	
## **Recommended Documents**

* [Field mappings and transformations using Azure Search indexers](https://docs.microsoft.com/azure/search/search-indexer-field-mappings) 
