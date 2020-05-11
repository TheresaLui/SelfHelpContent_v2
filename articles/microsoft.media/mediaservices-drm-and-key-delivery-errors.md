<properties
	pageTitle="DRM encryption and key delivery errors"
	description="DRM encryption and key delivery errors"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-drm-and-key-delivery-errors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632092"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# DRM encryption and key delivery errors 

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.<br>
Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

Before implementing DRM encryption, review [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview). It is highly recommended to focus and fully test each part described in the [Main components of a content protection system](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview#main-components-of-a-content-protection-system) section before moving onto the next part. To test your "content protection" system, use the tools specified in the section.

To get details on all failing Key delivery service request, enable the Azure monitoring diagnostic logs. For more information, see [Monitor Media Services metrics and diagnostic logs](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs).

If you get **MPE_ENC_ENCRYPTION_NOT_SET_IN_DELIVERY_POLICY**, make sure you specified the appropriate [Streaming Policy](https://docs.microsoft.com/azure/media-services/latest/streaming-policy-concept).

If you get errors that end with "**_NOT_SPECIFIED_IN_URL**", make sure that you specify the encryption format in the URL (for example, `…/manifest (format=m3u8-cmaf,encryption=cbcs-aapl)`). For details, see [Streaming protocols and encryption types](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview#streaming-protocols-and-encryption-types).

## **Recommended Documents**

* [Design of a multi-DRM content protection system with access control](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control)<br>
* [FAQs](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control#faqs)<br>
* [Tutorial: Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-aes128)<br>
* [How-to: Use DRM dynamic encryption and license delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-drm)<br>
* [Offline FairPlay Streaming for iOS](https://docs.microsoft.com/azure/media-services/latest/offline-fairplay-for-ios)<br>
* [Offline Widevine streaming for Android](https://docs.microsoft.com/azure/media-services/latest/offline-widevine-for-android)<br>
* [Offline PlayReady Streaming for Windows 10](https://docs.microsoft.com/azure/media-services/latest/offline-plaready-streaming-for-windows-10)
