<properties
	pageTitle="Search Index/I’m not getting the search results I expected"
	description="Understanding how Azure Cognitive Search ranks search results"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="2"
	supportTopicIds="32681348"
	resourceTags=""
	productPesIds="15568"
	articleId="search-results-unexpected"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Understanding how Azure Cognitive Search ranks search results

## **Recommended Steps**

 For text queries, Azure Cognitive Search will seamlessly deliver expected results in most scenarios, but occasionally you might get a result that seems "off" somehow. In these situations, having a background in the four stages of Lucene query execution (query parsing, lexical analysis, document matching, scoring) can help you identify specific changes to query parameters or index configuration that will deliver the desired outcome.  For more details on this, please review the following document:
 
* [How full text search works in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-lucene-query-architecture)

For more information, please also refer to:
* [Search Documents REST API](https://docs.microsoft.com/rest/api/searchservice/search-documents)
* [Simple query syntax](https://docs.microsoft.com/rest/api/searchservice/simple-query-syntax-in-azure-search)
* [Full Lucene query syntax](https://docs.microsoft.com/rest/api/searchservice/lucene-query-syntax-in-azure-search)
* [Handle search results](https://docs.microsoft.com/azure/search/search-pagination-page-layout)

## **Recommended Documents**

* [How full text search works in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-lucene-query-architecture)
* [Search Documents REST API](https://docs.microsoft.com/rest/api/searchservice/search-documents)
* [Simple query syntax](https://docs.microsoft.com/rest/api/searchservice/simple-query-syntax-in-azure-search)
* [Full Lucene query syntax](https://docs.microsoft.com/rest/api/searchservice/lucene-query-syntax-in-azure-search)
* [Handle search results](https://docs.microsoft.com/azure/search/search-pagination-page-layout)

