<properties
	pageTitle="DRM encryption and key delivery"
	description="DRM encryption and key delivery"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-drm-and-key-delivery"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632068"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# DRM encryption and key delivery

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.<br>
Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

Before implementing DRM encryption, review [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview). It is highly recommended to focus and fully test each part described in the [Main components of a content protection system](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview#main-components-of-a-content-protection-system) section before moving onto the next part. To test your "content protection" system, use the tools specified in the section.

To get details on all failing Key delivery service requests, enable the Azure monitoring diagnostic logs. For more information, see [Monitor Media Services metrics and diagnostic logs](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs).

If you need to implement offline mode playback, see the following articles:<br>
* [Offline FairPlay Streaming for iOS](https://docs.microsoft.com/azure/media-services/latest/offline-fairplay-for-ios)
* [Offline Widevine streaming for Android](https://docs.microsoft.com/azure/media-services/latest/offline-widevine-for-android)<br>
* [Offline PlayReady Streaming for Windows 10](https://docs.microsoft.com/azure/media-services/latest/offline-plaready-streaming-for-windows-10)

Offline download/playback of files encrypted with AES-128 is not supported by Media Services.

## **Recommended Documents**

**Concepts**

* [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)<br>
* [Design of a multi-DRM content protection system with access control](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control)<br>
* [Streaming Policies](https://docs.microsoft.com/azure/media-services/latest/streaming-policy-concept)<br>
* [Content Key Policies](https://docs.microsoft.com/azure/media-services/latest/content-key-policy-concept)<br>
* [FAQs](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control#faqs)

**Tutorials and how-tos**

* [Tutorial: Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-aes128)<br>
* [Use DRM dynamic encryption and license delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-drm)<br>
* [Get a signing key from the existing policy](https://docs.microsoft.com/azure/media-services/latest/get-content-key-policy-dotnet-howto)<br>
