<properties
	pageTitle="Azure Media Player closed captions and subtitle support"
	description="Azure Media Player closed captions and subtitle support"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-player-closed-captions"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632086"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Player closed captions and subtitles

At this time, Azure Media Player currently supports captions for only On Demand events with WebVTT format and live events using CEA-708 pass-through. IMSC1/TTML format is currently unsupported. Captions and subtitles allow the player to cater to and empower a broader audience, including people with hearing disabilities or those who want to read along in a different language. Captions also increase video engagement, improve comprehension, and make it possible to view the video in sound sensitive environments, like a workplace.

### **Sample WebVTT Subtitles in Azure Media Player**

Please review [this sample of using WebVTT](https://amp.azure.net/libs/amp/latest/samples/dynamic_webvtt.html) subtitles with Azure Media Player. 

### **Live captions with 608/708 pass-through**

Please review [this sample showing live captions with 608/708 passthrough](https://amp.azure.net/libs/amp/latest/samples/dynamic_live_captions.html).

Your upstream live encoder must be capable of pre-inserting CEA-708 and 608 captions into the video stream. If captions are detected in the video stream, they will be preserved. 

## **Recommended Documents**

* [Subtitle and Captions in Azure Media Player](http://amp.azure.net/libs/amp/latest/docs/index.html#captions-and-subtitles)<br> 
* [CEA-708 and 608 captions settings in Player](http://amp.azure.net/libs/amp/latest/docs/index.html#amp.player.cea708captionssettings)<br>
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)<br>
* [Azure Media Player changelog](http://amp.azure.net/libs/amp/latest/docs/changelog.html)


