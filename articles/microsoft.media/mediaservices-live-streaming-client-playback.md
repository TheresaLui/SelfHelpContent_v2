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
	cloudEnvironments="public"
/>

# Client playback

**NOTE:** For explanations about operations that needed to be performed on the Media Services side, before your client can playback your videos, this topic references Media Services v3 API documentation. v3 is the latest Media Services version.

To make videos in the output Asset available to clients for playback, you have to create a [Streaming Locator](https://docs.microsoft.com/azure/media-services/latest/streaming-locators-concept) and then build streaming URLs. For .NET sample, see [Get a Streaming Locator](stream-files-tutorial-with-api.md#get-a-streaming-locator).

**Live captions with 608/708 pass-through**

Please review [this sample showing live captions with 608/708 passthrough](https://amp.azure.net/libs/amp/latest/samples/dynamic_live_captions.html).

Your upstream live encoder must be capable of pre-inserting CEA-708 and 608 captions into the video stream. If captions are detected in the video stream, they will be preserved. 

**Browsers and OS support**

If you are using Azure Media Player, see the [browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix) for the player.

**FAQs**

Q: How do I check if my browser supports Media Source Extensions?

A: For modern streaming playback for work (DASH, HLS) your browser should support Media Source Extension. See the ["Can I Use" website](https://caniuse.com/#feat=mediasource).

Q: How do I check if my browser supports Encrypted Media Extensions?

A: For DRM content to playback, check the support matrix for EME on the browser and confirm the proper DRM is configured for targeting that browser. See the ["Can I Use" website](https://caniuse.com/#feat=eme).

Q: Does my browser or target device support HEVC/H.265 video playback?

A: See the ["Can I Use" website](https://caniuse.com/#feat=hevc). If you are looking for device support of HEVC, please check with the device manufacturer to determine which hardware releases include support for HEVC playback.  

Q: Apple iOS and HEVC

A: For iOS devices, HEVC playback was included in iOS 11.0 or higher: iPhone X, iPhone 8/Plus, iPhone 7/6s/6/Plus. Not all phone models are capable of playing back 4K and may be limited to specific resolutions and frame rate requirements. For example, iPhone 6/Plus can play HEVC video only up to 1080p at 240fps. iPhone XS/XR/X, iPhone 8/Plus, iPhone 7/6s/Plus with Apples A9, A10 chipset (or later) support up to 4K 2160p playback at common framerates. <br>For details on supported Apple devices for HEVC, please search HEVC in the [Apple support system](https://support.apple.com/kb/index?page=search&q=HEVC&product=&doctype=SPECIFICATIONS&currentPage=1&includeArchived=false&locale=en_US).

Q: Android and HEVC

A: Android supports HEVC in Android 5.0+ on certain OEM hardware. 

- Chromecast Ultra supports HEVC
- Android mobile has support for HEVC, but typically only up to Main Level 3 on mobile devices (very limited support in market). See [video formats and codecs supported by Android mobile.](https://developer.android.com/guide/topics/media/media-formats#video-codecs).
- Android TV support for HEVC up to Main Level 4.1. See [video formats and codecs supported by Android TV](https://developer.android.com/guide/topics/media/media-formats#video-codecs) for details. 

Q: Does my browser support H.264/AVC video playback?

A: See the ["Can I Use" website](https://caniuse.com/#feat=mpeg4).

Q: Why will my video not play back on a specific Android model?

A: Successful playback on Android devices requires a combination of device capabilities, graphics support, codec rendering, OS support and more. Since Android is an open source platform which allows phone manufacturers to change the base Android OS provided by Google, this caused fragmentation in the Android compatibility for video and audio playback and some devices may not be supported because of a lack in features. As well, some Android devices do not have support for all popular codecs (HEVC, AAC, H.264).

## **Recommended Documents**

* [Dynamic packaging](https://docs.microsoft.com/azure/media-services/latest/dynamic-packaging-overview)<br>
* [Dynamic manifests](https://docs.microsoft.com/azure/media-services/latest/filters-dynamic-manifest-overview)<br>
* [Content protection with dynamic encryption](https://docs.microsoft.com/azure/media-services/latest/content-protection-overview)
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
