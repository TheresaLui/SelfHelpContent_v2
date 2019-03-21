<properties
	pageTitle="Live streaming with a live cloud encoder"
	description="Live streaming with a live cloud encoder"
	infoBubbleText=""
	service="microsoft.media"
	resource="liveevent"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-live-streaming-live-cloud-encoder"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632105"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Live streaming with a live cloud encoder

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

When using live encoding with Media Services, you would configure your on-premises live encoder to send a single bitrate video as the contribution feed to the Live Event (using RTMP or Fragmented-Mp4 protocol). The Live Event encodes that incoming single bitrate stream to a [multiple bitrate video stream](https://en.wikipedia.org/wiki/Adaptive_bitrate_streaming), makes it available for delivery to play back devices via protocols like MPEG-DASH, HLS, and Smooth Streaming. When creating this type of Live Event, specify the encoding type as **Standard** (LiveEventEncodingType.Standard).

You can send the contribution feed at up to 1080p resolution at a frame rate of 30 frames/second, with H.264/AVC video codec and AAC (AAC-LC, HE-AACv1, or HE-AACv2) audio codec. See the [Live Event types comparison](https://docs.microsoft.com/azure/media-services/latest/live-event-types-comparison) article for more details.

When using live encoding (Live Event set to **Standard**), the encoding preset defines how the incoming stream is encoded into multiple bitrates or layers. For information, see [System presets](https://docs.microsoft.com/azure/media-services/latest/live-event-types-comparison#system-presets).

Currently, the only allowed preset value for the Standard type of Live Event is *Default720p*. If you need to use a custom live encoding preset, please contact amshelp@microsoft.com. You should specify the desired table of resolution and bitrates. Do verify that there is only one layer at 720p, and at most 6 layers.

## **Recommended Documents**

* [Recommended live encoders to use with Media Services](https://docs.microsoft.com/azure/media-services/latest/recommended-on-premises-live-encoders)<br>
* [Overview of live streaming with the v3 API](https://docs.microsoft.com/azure/media-services/latest/live-streaming-overview)
* [Live Events and Live Outputs](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)
* [States and billing](https://docs.microsoft.com/azure/media-services/latest/live-event-states-billing)
