<properties
	pageTitle="Issues encrypting with FairPlay"
	description="Issues encrypting with FairPlay"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-drm-and-key-delivery-fairplay-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632095"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Issues encrypting with FairPlay

**Media Services v3 (latest)**

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).
 
Before implementing DRM encryption, review [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview). It is highly recommended to focus and fully test each part described in the [Main components of a content protection system](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview#main-components-of-a-content-protection-system) section before moving onto the next part. To test your "content protection" system, use the tools specified in the section.

To get details on all failing Key delivery service request, enable the Azure monitoring diagnostic logs. For more information, see [Monitor Media Services metrics and diagnostic logs](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs).

To specify the Fairplay encryption Streaming Policy, use the "Predefined_MultiDrmStreaming". For an example of how to configure a Fairplay Content Key Policy option, see [Create Content Key Policies](https://github.com/Azure-Samples/media-services-v3-dotnet-tutorials/blob/master/AMSV3Tutorials/EncryptWithDRM/Program.cs#L180)

Concepts:

* [Apple FairPlay license requirements and configuration](https://docs.microsoft.com/azure/media-services/latest/fairplay-license-overview)<br>
* [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)<br>
* [Design of a multi-DRM content protection system with access control](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control)<br>
* [Streaming Policies](https://docs.microsoft.com/azure/media-services/latest/streaming-policy-concept)<br>
* [Content Key Policies](https://docs.microsoft.com/azure/media-services/latest/content-key-policy-concept)<br>
* [FAQs](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control#faqs)<br>

Tutorials and how-tos:

* [Tutorial: Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-aes128)<br>
* [Use DRM dynamic encryption and license delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-drm)<br>
* [Get a signing key from the existing policy](https://docs.microsoft.com/azure/media-services/latest/get-content-key-policy-dotnet-howto)<br>
* [Offline FairPlay Streaming for iOS](https://docs.microsoft.com/azure/media-services/latest/offline-fairplay-for-ios)

## **Recommended Documents**

* [Apple FairPlay license requirements and configuration](https://docs.microsoft.com/azure/media-services/latest/fairplay-license-overview) (v3)<br>
* [Protect your HLS content with Apple FairPlay or Microsoft PlayReady](https://docs.microsoft.com/azure/media-services/previous/media-services-protect-hls-with-fairplay) (v2)