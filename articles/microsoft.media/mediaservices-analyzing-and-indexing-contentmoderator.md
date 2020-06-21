<properties
	pageTitle="Azure Media Services analyzing with content moderator"
	description="Azure Media Services analyzing with content moderator"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-analyzing-and-indexing-contentmoderator"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632087"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Services analyzing with content moderator

Content Moderator is available as a standalone analyzer in the v2 API only. The Azure Media Content Moderator media processor (MP) enables you to use machine-assisted moderation for your videos. For example, you might want to detect possible adult and racy content in videos and review the flagged content by your human moderation teams.

### Is the Content Moderator in the legacy v2 API Preview only?
The Azure Media Content Moderator processor exposed in the legacy v2 API is currently in Preview and only available via the v2 API for Media Services.  For customers looking for a production (GA) ready API, we recommend to use the [Video Indexer API](http://video.ai) directly. 

### Using the v3 API or Video Indexer API for content moderation

Azure Media Services v3 enables you to extract insights from your video and audio files with Video Indexer through AMS v3 analyzer presets. If you want more detailed insights, use Video Indexer APIs directly. To understand when you would want to use Video Indexer vs. Media Services analyzer presets, check out the [comparison document](https://docs.microsoft.com/azure/media-services/video-indexer/compare-video-indexer-with-media-services-presets).

### Where can I find content moderation output in the Video Indexer API?

The content moderation results are output to the Video Indexer JSON file in the [visualContentModeration](https://docs.microsoft.com/azure/media-services/video-indexer/video-indexer-output-json-v2#visualcontentmoderation) and [textualContentModeration](https://docs.microsoft.com/azure/media-services/video-indexer/video-indexer-output-json-v2#textualcontentmoderation) sections. 
For details see the article [Video Indexer output JSON](https://docs.microsoft.com/azure/media-services/video-indexer/video-indexer-output-json-v2)

## **Recommended Documents**

* [Azure Media Content Moderator usage in the legacy v2 API](https://docs.microsoft.com/azure/media-services/previous/media-services-content-moderation)
* [Video Indexer API support for content moderation](https://docs.microsoft.com/azure/media-services/video-indexer/video-indexer-output-json-v2)
* [Tutorial: Analyze videos with Azure Media Services](https://docs.microsoft.com/azure/media-services/latest/analyze-videos-tutorial-with-api)
* [Scale media analytics and indexing](https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview).
* [Video Indexer Developer Portal and APIs](https://api-portal.videoindexer.ai/)


