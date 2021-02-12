<properties
	pageTitle="Archiving a live stream"
	description="Archiving a live stream"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-live-streaming-archiving"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632078"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Archiving a live stream

**Media Services v3 (latest)**

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

Before you start developing live streaming applications with Media Services v3, review [Live Events and Live Outputs](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)

When using Media Services v3 API, one of the steps in a live streaming workflow is to create a Live Event and a Live Output. The Live Output is associated with an Asset into which your live stream is being archived. Live Output makes your stream available to viewers through the Streaming Endpoint.

The relationship between a Live Event and its Live Outputs is similar to traditional television broadcast, whereby a channel (Live Event) represents a constant stream of video and a recording (Live Output) is scoped to a specific time segment (for example, evening news from 6:30PM to 7:00PM). You can record television using a Digital Video Recorder (DVR) – the equivalent feature in Live Events is managed via the **ArchiveWindowLength** property. For more information, see [Using a cloud DVR](https://docs.microsoft.com/azure/media-services/latest/live-event-cloud-dvr)

**Media Services v2 (legacy)**

In Media Services v2, Channels are responsible for processing live streaming content. A Program enables you to control the publishing and storage of segments in a live stream. Channels manage Programs. A program is scoped to some timed event on the channel on which it is running. You can specify the number of hours you want to retain the recorded content for the program by setting the ArchiveWindowLength property. This value can be set from a minimum of 5 minutes to a maximum of 25 hours. For more information, see [Description of a Channel and its related components](https://docs.microsoft.com/azure/media-services/previous/media-services-manage-channels-overview#description-of-a-channel-and-its-related-components).

## **Recommended Documents**

* [Using a cloud DVR](https://docs.microsoft.com/azure/media-services/latest/live-event-cloud-dvr)
