<properties
	pageTitle="Manage Azure Media Services quotas"
	description="Manage Azure Media Services quotas"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-quotas"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632070"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Manage Azure Media Services quotas

There are quotas and limitations associated with an Azure Media Services account. Some limits are fixed, in which case they cannot be increased. The following list contains the default (soft) limits that could be increased by opening a support ticket. Make sure to include detailed information in the request on the desired quota changes, use-case scenarios, and regions required.

| Resource | Default Limit | 
| --- | --- | 
| Assets per Azure Media Services account | 1,000,000|
| Dynamic Manifest Filters|100|
| Listing Transforms|Paginate the response, with 1000 Transforms per page|
| Listing Jobs|Paginate the response, with 500 Jobs per page|
| Live Events per Media Services account |5|
| Live Outputs in running state per LiveEvent |3|
| Streaming Policies | 100 |
| Content Key Policy |30 | 

## **Recommended Documents**

* [Azure Media Services v3 quotas and limitations](https://docs.microsoft.com/azure/media-services/latest/limits-quotas-constraints) <br>
* [Media Services v2 (legacy) quotas and limitations](https://docs.microsoft.com/azure/media-services/previous/media-services-quotas-and-limitations)
