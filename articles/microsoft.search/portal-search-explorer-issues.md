<properties
	pageTitle="Portal/Search Explorer issues"
	description="Issues with Azure Cognitive Search portal search explorer"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="3"
	supportTopicIds="32681383"
	resourceTags=""
	productPesIds="15568"
	articleId="portal-search-explorer-issues"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issues with Azure Cognitive Search portal search explorer

## **Recommended Steps**

If you are having issues with the search explorer within the portal for Azure Cognitive Search, here are the most common reasons:

* Long timeframe for response:  Azure Cognitive Search returns 50 documents in a search result.  If your documents contain a lot of data (such as text indexed from a PDF), it can take a long time to load the results into the search explorer.  You can optimize this, by limiting the fields returned ([select](https://docs.microsoft.com/azure/search/search-pagination-page-layout#total-hits-and-page-counts)) or by limiting the documents that are returned ([top](https://docs.microsoft.com/azure/search/search-pagination-page-layout#total-hits-and-page-counts))
* Portal showing cloud: This indicates a temporary issue with access to the Azure Portal.  In most cases, reloading the page will solve the issue.  If the problem persists, please check the [Azure Status](https://status.azure.com) page for potential other issues

## **Recommended Documents**

* [Using the Search Query Explorer](https://docs.microsoft.com/azure/search/search-explorer)
* [Total hits and Page Counts](https://docs.microsoft.com/azure/search/search-pagination-page-layout#total-hits-and-page-counts)
* [Azure Status](https://status.azure.com)
