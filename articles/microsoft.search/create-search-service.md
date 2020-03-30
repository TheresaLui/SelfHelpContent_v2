<properties
	pageTitle="Issue creating a search service"
	description="Issue creating a search service"
	service="microsoft.search"
	resource="searchservices"
	authors="cynotebo"
	ms.author="cynotebo"
	selfHelpType="resource"
	displayOrder="80"	
	supportTopicIds="32681355"
	resourceTags=""
	productPesIds="15568"
	articleId="create-search-service"
	cloudEnvironments="public, Fairfax"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating a search service

## Azure capacity restrictions related to COVID-19

In response to health authorities emphasizing the importance of social distancing, we are supporting businesses, schools, and governments in the unprecedented mobilization of remote workforces. As expected, we've seen significant usage increases in services that support these workloads – including Microsoft Teams, Windows Virtual Desktop, and Azure Media Services.  For more information, please read the blog post about [our commitment to service continuity](https://azure.microsoft.com/blog/our-commitment-to-customers-and-microsoft-cloud-services-continuity/) while we all come together to battle a global pandemic.

As demand continues to grow, we are faced with temporary capacity constraints in a number of Azure regions. As a result, customers are currently unable to use the portal to create new Azure Cognitive Search services in the following regions: **UK South, France Central, North Europe, UAE North, Central India**

At this time we request that you create your search service in a different region. We apologize for any inconvenience this causes and expect this situation to improve in the coming months, but is, of course, contigent on the resolution of general capacity constraints across Azure.

## **Recommended Steps**

If you are having trouble creating an Azure Cognitive Search service, you may want to ensure that:

1.	You have access to create resources within your Azure subscription
2.	You have provided a unique name for your search service and followed the naming guidelines found [here](https://docs.microsoft.com/azure/search/search-create-service-portal)
3.	You have selected a [supported region](https://azure.microsoft.com/pricing/details/search/) for Azure Cognitive Search
4.	You have allowed adequate time for the Azure Cognitive Search service to be deployed. This typically occurs within minutes and can be monitored through Azure notifications.
5.	You have not already used your allotted number of free search services.  By default, each subscription is allowed only one free search service.

## **Recommended Documents**

* [Quickstart: Create an Azure Cognitive Search service in the portal](https://docs.microsoft.com/azure/search/search-create-service-portal)
* [Azure Search service quick start template](https://github.com/Azure/azure-quickstart-templates/tree/master/101-azure-search-create)
