<properties
	pageTitle="Client playback"
	description="Client playback"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-live-streaming-client-playback"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632085"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Client playback

**Live captions with 608/708 pass-through**

Please review [this sample showing live captions with 608/708 passthrough](https://amp.azure.net/libs/amp/latest/samples/dynamic_live_captions.html).

Your upstream live encoder must be capable of pre-inserting CEA-708 and 608 captions into the video stream. If captions are detected in the video stream, they will be preserved. 

**Browsers and OS support**

If you are using Azure Media Player, see the [browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix) for the player.

**How do I check if my browser supports Media Source Extensions?**

For modern streaming playback for work (DASH, HLS) your browser should support Media Source Extension. See the ["Can I Use" website](https://caniuse.com/#feat=mediasource).

**How do I check if my browser supports Encrypted Media Extensions?**

For DRM content to playback, check the support matrix for EME on the browser and confirm the proper DRM is configured for targeting that browser. See the ["Can I Use" website](https://caniuse.com/#feat=eme).

**Does my browser or target device support HEVC/H.265 video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=hevc). If you are looking for device support of HEVC, please check with the device manufacturer to determine which hardware releases include support for HEVC playback.  

**Apple iOS and HEVC**

For iOS devices, HEVC playback was included in iOS 11.0 or higher: iPhone X, iPhone 8/Plus, iPhone 7/6s/6/Plus. Not all phone models are capable of playing back 4K and may be limited to specific resolutions and frame rate requirements. For example, iPhone 6/Plus can play HEVC video only up to 1080p at 240fps. iPhone XS/XR/X, iPhone 8/Plus, iPhone 7/6s/Plus with Apples A9, A10 chipset (or later) support up to 4K 2160p playback at common framerates. <br>For details on supported Apple devices for HEVC, please search HEVC in the [Apple support system](https://support.apple.com/kb/index?page=search&q=HEVC&product=&doctype=SPECIFICATIONS&currentPage=1&includeArchived=false&locale=en_US).

**Android and HEVC**

Android supports HEVC in Android 5.0+ on certain OEM hardware. 

- Chromecast Ultra supports HEVC
- Android mobile has support for HEVC, but typically only up to Main Level 3 on mobile devices (very limited support in market). See [video formats and codecs supported by Android mobile.](https://developer.android.com/guide/topics/media/media-formats#video-codecs).
- Android TV support for HEVC up to Main Level 4.1. See [video formats and codecs supported by Android TV](https://developer.android.com/guide/topics/media/media-formats#video-codecs) for details. 

**Does my browser support H.264/AVC video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=mpeg4).

**Why will my video not play back on a specific Android model?**

Successful playback on Android devices requires a combination of device capabilities, graphics support, codec rendering, OS support and more. Since Android is an open source platform which allows phone manufacturers to change the base Android OS provided by Google, this caused fragmentation in the Android compatibility for video and audio playback and some devices may not be supported because of a lack in features. As well, some Android devices do not have support for all popular codecs (HEVC, AAC, H.264).

## **Recommended Documents**

**Media Services v3 (latest)**

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

When using Media Services v3, to make videos in the output Asset available to clients for playback, you have to create a [Streaming Locator](https://docs.microsoft.com/azure/media-services/latest/streaming-locators-concept) and then build streaming URLs. For .NET sample, see [Get a Streaming Locator](stream-files-tutorial-with-api.md#get-a-streaming-locator).

* [Streaming Endpoint](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept)<br>
* [Dynamic packaging](https://docs.microsoft.com/azure/media-services/latest/dynamic-packaging-overview)<br>
* [Dynamic manifests](https://docs.microsoft.com/azure/media-services/latest/filters-dynamic-manifest-overview)<br>
* [Content protection with dynamic encryption](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>

**Media Services v2 (letacy)**

When using Media Services v2, to make videos in the output Asset available to clients for playback, you have to create a Locator and then build streaming URLs. For more information, see [Deliver content to customers](https://docs.microsoft.com/azure/media-services/previous/media-services-deliver-content-overview).