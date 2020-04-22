<properties
	pageTitle="Azure Media Services analyzing and indexing files"
	description="Azure Media Services analyzing and indexing files"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-analyzing-and-indexing"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632062"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Services analyzing and indexing files

### Analyzing and Indexing files
Azure Media Services enables you to extract insights from your video and audio files with Video Indexer through AMS v3 analyzer presets. If you want more detailed insights, use the [Video Indexer APIs](https://api-portal.videoindexer.ai/) directly. To understand when you would want to use Video Indexer vs. Media Services analyzer presets, check out the [comparison document](https://docs.microsoft.com/azure/media-services/video-indexer/compare-video-indexer-with-media-services-presets).


### Recommended Steps to analyze your video and audio files in Azure Media Services


*  To analyze your content using Media Services v3 presets, you create a Transform and submit a Job that uses one of these presets: VideoAnalyzerPreset or AudioAnalyzerPreset. 
*  The following tutorial demonstrates how to use the [VideoAnalyzerPreset](https://docs.microsoft.com/rest/api/media/transforms/createorupdate#videoanalyzerpreset):
   *  [Tutorial: Analyze videos with Azure Media Services](https://docs.microsoft.com/azure/media-services/latest/analyze-videos-tutorial-with-api)


### Troubleshoot slow audio and video indexing


* When using a Video or Audio Analyzer presets, use the Azure portal or the CLI to set your account to have at least  10 "S3" Media Reserved Units. For more information, see [Scale media analytics and indexing](https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview).

## **Recommended Documents**

* [Analyzing video and audio files overview](https://docs.microsoft.com/azure/media-services/latest/analyzing-video-audio-files-concept)
* [Tutorial: Analyze videos with Azure Media Services](https://docs.microsoft.com/azure/media-services/latest/analyze-videos-tutorial-with-api)
* [Scale media analytics and indexing](https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview).
* [Video Indexer Developer Portal and APIs](https://api-portal.videoindexer.ai/)
* [Pricing page for analytics and indexing (see Analytics & Indexing tab)](https://azure.microsoft.com/pricing/details/media-services/)

