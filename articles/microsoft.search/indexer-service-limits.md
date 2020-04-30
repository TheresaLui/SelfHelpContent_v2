<properties
	pageTitle="Issue or question on indexer service limits"
	description="Issue or question on indexer service limits"
	service="microsoft.search"
	resource="searchservices"
	authors="vkurpad"
	ms.author="vikurpad"
	selfHelpType="resource"
	displayOrder="16"	
	supportTopicIds="32681382"
	resourceTags=""
	productPesIds="15568"
	articleId="indexer-service-limits"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>
# Issue or question on indexer service limits

## **Recommended Steps**

If your indexer did not complete indexing all your content successfully, you may want to:

1. Look at the Azure Search [service limits](https://docs.microsoft.com/azure/search/search-limits-quotas-capacity)
1. Note than an single indexer run will stop after 24 hours of activity. If indexing your content requires more than 24 hours of indexing activity, you will need to set an [indexer schedule](https://docs.microsoft.com/azure/search/search-howto-schedule-indexers). That will trigger additional runs on a recurring basis.   AI Enrichment workloads and image analysis in Azure blob indexing have shorter running times than regular text indexing (2 hours instead of 24 hours), but setting a schedule will help you get around this limitation.
1. Check the SKU tier and replicas you have provisioned

## **Recommended Documents**

* [Service limits in Azure Search](https://docs.microsoft.com/azure/search/search-limits-quotas-capacity#indexer-limits) 
* [How to schedule indexers](https://docs.microsoft.com/azure/search/search-howto-schedule-indexers)
