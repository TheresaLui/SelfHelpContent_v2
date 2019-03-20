<properties
	pageTitle="Issues encrypting with PlayReady"
	description="Issues encrypting with PlayReady"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-drm-and-key-delivery-playready-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632112"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Issues encrypting with PlayReady

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

Before implementing DRM encryption, review [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview). It is highly recommended to focus and fully test each part described in the [Main components of a content protection system](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview#main-components-of-a-content-protection-system) section before moving onto the next part. To test your "content protection" system, use the tools specified in the section.

To get details on all failing Key delivery service request, enable the Azure monitoring diagnostic logs. For more information, see [Monitor Media Services metrics and diagnostic logs](https://docs.microsoft.com/azure/media-services/latest/media-services-metrics-diagnostic-logs).

To specify the PlayReady encryption Streaming Policy, use the "Predefined_MultiDrmCencStreaming". The "Predefined_MultiDrmCencStreaming" policy supports envelope and cenc encryption and sets two content keys on the Streaming Locator. For an example of how to configure a PlayReady Content Key Policy option, see [Create Content Key Policies](https://github.com/Azure-Samples/media-services-v3-dotnet-tutorials/blob/master/AMSV3Tutorials/EncryptWithDRM/Program.cs#L180)

## **Recommended Documents**

**Concepts**

* [Content protection overview](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)<br>
* [Design of a multi-DRM content protection system with access control](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control)<br>
* [Streaming Policies](https://docs.microsoft.com/azure/media-services/latest/streaming-policy-concept)<br>
* [Content Key Policies](https://docs.microsoft.com/azure/media-services/latest/content-key-policy-concept)<br>
* [Media Services PlayReady license template](https://docs.microsoft.com/azure/media-services/latest/playready-license-template-overview)<br>
* [FAQs](https://docs.microsoft.com/azure/media-services/latest/design-multi-drm-system-with-access-control#faqs)<br>

**Tutorials and how-tos**

* [Tutorial: Use AES-128 dynamic encryption and the key delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-aes128)<br>
* [Use DRM dynamic encryption and license delivery service](https://docs.microsoft.com/azure/media-services/latest/protect-with-drm)<br>
* [Get a signing key from the existing policy](https://docs.microsoft.com/azure/media-services/latest/get-content-key-policy-dotnet-howto)<br>
* [Offline PlayReady Streaming for Windows 10](https://docs.microsoft.com/azure/media-services/latest/offline-plaready-streaming-for-windows-10)
