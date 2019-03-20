<properties
	pageTitle="Live streaming with on-premises encoder"
	description="Live streaming with on-premises encoder"
	infoBubbleText=""
	service="microsoft.media"
	resource="liveevent"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-live-streaming-onpremises-encoders"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632108"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Live streaming with on-premises encoder

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

When using the pass-through **Live Event**, you rely on your on-premises live encoder to generate a multiple bitrate video stream and send that as the contribution feed to the Live Event (using RTMP or fragmented-MP4 protocol). The Live Event then carries through the incoming video streams without any further processing. Such a pass-through LiveEvent is optimized for long-running live events or 24x365 linear live streaming. When creating this type of Live Event, specify None (LiveEventEncodingType.None).

You can send the contribution feed at resolutions up to 4K and at a frame rate of 60 frames/second, with either H.264/AVC or H.265/HEVC video codecs, and AAC (AAC-LC, HE-AACv1, or HE-AACv2) audio codec.  See the [Live Event types comparison](https://docs.microsoft.com/azure/media-services/latest/live-event-types-comparison) article for more details.

**NOTE:** Using a pass-through method is the most economical way to do live streaming when you are doing multiple events over a long period of time, and you have already invested in on-premises encoders. See [pricing](https://azure.microsoft.com/pricing/details/media-services/) details.

## **Recommended Documents**

* [Recommended live encoders to use with Media Services](https://docs.microsoft.com/azure/media-services/latest/recommended-on-premises-live-encoders)<br>
* [Overview of live streaming with the v3 API](https://docs.microsoft.com/azure/media-services/latest/live-streaming-overview)
* [Live Events and Live Outputs](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)
* [Live streaming tutorial with .NET](https://docs.microsoft.com/azure/media-services/latest/stream-live-tutorial-with-api)
* [States and billing](https://docs.microsoft.com/azure/media-services/latest/live-event-states-billing)
