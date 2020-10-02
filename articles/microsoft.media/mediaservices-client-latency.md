<properties
	pageTitle="Client Latency"
	description="Client Latency"
	service="microsoft.media"
	resource="mediaservices"
	authors="akucer"
	ms.author="akucer"
	displayOrder="1"
	articleId="mediaservices-client-latency"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32729550,32632085"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, mooncake, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Client Latency

## **Recommended Steps** 

* Ensure you are using Azure Media Services in an Azure region that is geographically closest to the majority of your customers
* Enable Azure CDN for your streaming endpoint if a large number of clients will be simultaneously accessing content. Azure CDN can be enabled directly using either media services APIs or the Azure Portal.
* For live streaming use a [recommended on-premises encoder](https://docs.microsoft.com/azure/media-services/previous/media-services-recommended-encoders)
* Pre-load the media player on your webpage

## **Recommended Documents**

* [Live event low latency settings](https://docs.microsoft.com/azure/media-services/latest/live-event-latency)
