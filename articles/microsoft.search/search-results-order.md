<properties
	pageTitle="My search results are not in correct order"
	description="My search results are not in correct order"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="52"	
	supportTopicIds="32681380"
	resourceTags=""
	productPesIds="15568"
	articleId="search-results-order"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# My search results are not in correct order

## **Recommended Steps**

Azure Cognitive Search computes a search score for each item in an ordered result set and every item in the search results set is assigned a search score, then ranked highest to lowest based on the scores calculated for each item.  The score is an indicator of an item's relevance in the context of the current search operation. The higher the score, the more relevant the item. 

[Scoring profiles](https://docs.microsoft.com/azure/search/index-add-scoring-profiles) give you greater control over the ranking of items in search results and allow you to customize the scoring calculation.

## **Recommended Documents**

* [Add scoring profiles to an Azure Cognitive Search index](https://docs.microsoft.com/azure/search/index-add-scoring-profiles)
