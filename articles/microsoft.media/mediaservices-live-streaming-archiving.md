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
	cloudEnvironments="public"
/>

# Archiving a live stream

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

Before you start developing live streaming applications with Media Services v3, review [Live Events and Live Outputs](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)

When using Media Services v3 API, one of the steps in a live streaming workflow is to create a Live Event and a Live Output. The Live Output is associated with an Asset into which your live stream is being archived. Live Output makes your stream available to viewers through the Streaming Endpoint.

The relationship between a Live Event and its Live Outputs is similar to traditional television broadcast, whereby a channel (Live Event) represents a constant stream of video and a recording (Live Output) is scoped to a specific time segment (for example, evening news from 6:30PM to 7:00PM). You can record television using a Digital Video Recorder (DVR) – the equivalent feature in Live Events is managed via the **ArchiveWindowLength** property. 

## **Recommended Documents**

[Using a cloud DVR](https://docs.microsoft.com/azure/media-services/latest/live-event-cloud-dvr)
