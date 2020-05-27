<properties
	pageTitle="Issues encrypting with AES-128 clear key"
	description="Issues encrypting with AES-128 clear key"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-drm-and-key-delivery-aes-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632076"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
 
# Issues encrypting with AES-128 clear key

**Does offline playback work with AES-128 clear key encryption?**

 No. Offline download/playback of files encrypted with AES-128 is not supported by Media Services.
 
**Media Services v3 (latest)**
 
**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

To get details on all failing Key delivery service request, enable the Azure monitoring diagnostic logs. For more information, see [Monitor Media Services metrics and diagnostic logs](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs).

* [Concept: Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)<br>
* [FAQs](https://docs.microsoft.com/azure/media-services/latest/frequently-asked-questions#content-protection)<br>
* [Tutorial: Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-aes128)

**Media Services v2 (legacy)**

* [Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/previous/media-services-protect-with-aes128)

## **Recommended Documents**

[Concept: Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)
