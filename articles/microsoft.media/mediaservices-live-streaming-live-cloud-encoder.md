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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Live streaming with a live cloud encoder

When using live encoding with Media Services, you would configure your on-premises live encoder to send a single bitrate video as the contribution feed to the Channel (v2)/Live Event (v3) using RTMP or Fragmented-Mp4 protocol. The Channel/Live Event encodes that incoming single bitrate stream to a [multiple bitrate video stream](https://en.wikipedia.org/wiki/Adaptive_bitrate_streaming), makes it available for delivery to play back devices via protocols like MPEG-DASH, HLS, and Smooth Streaming. 

You can send the contribution feed at up to 1080p resolution at a frame rate of 30 frames/second, with H.264/AVC video codec and AAC (AAC-LC, HE-AACv1, or HE-AACv2) audio codec. See the [Live Event types comparison](https://docs.microsoft.com/azure/media-services/latest/live-event-types-comparison) article for more details.

When using live encoding, the encoding preset defines how the incoming stream is encoded into multiple bitrates or layers. For information, see [System presets](https://docs.microsoft.com/azure/media-services/latest/live-event-types-comparison#system-presets).

## **Recommended Documents**


**Media Services v3 (latest)**

* [Recommended live encoders to use with Media Services](https://docs.microsoft.com/azure/media-services/latest/recommended-on-premises-live-encoders)<br>
* [Overview of live streaming with the v3 API](https://docs.microsoft.com/azure/media-services/latest/live-streaming-overview)<br>
* [Live Events and Live Outputs](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)<br>
* [States and billing](https://docs.microsoft.com/azure/media-services/latest/live-event-states-billing)

**Media Services v2 (legacy)**

* [Live streaming with v2](https://docs.microsoft.com/azure/media-services/previous/media-services-manage-live-encoder-enabled-channels)

