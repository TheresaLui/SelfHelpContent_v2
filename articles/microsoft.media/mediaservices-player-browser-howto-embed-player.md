<properties
	pageTitle="Azure Media Player how to embed the player"
	description="Azure Media Player how to embed the player"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-player-howto-embed-player"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632099"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Player how to embed the player

### **Quick Start on embedding the player**

This section shows you the basic steps without going into details. Sections that follow give you specifics on how to set up and configure Azure Media Player. Simply add the following to your document's `<head>`:

```
<link href="//amp.azure.net/libs/amp/latest/skins/amp-default/azuremediaplayer.min.css" rel="stylesheet">
<script src= "//amp.azure.net/libs/amp/latest/azuremediaplayer.min.js"></script>
```

**IMPORTANT**: You should NOT use the latest version in production, as this is subject to change on demand. Replace latest with a version of Azure Media Player; for example replace latest with 1.0.0. Azure Media Player versions can be queried from here.

```
<video id="vid1" class="azuremediaplayer amp-default-skin" autoplay controls width="640" height="400" poster="poster.jpg" data-setup='{"nativeControlsForTouch": false}'>
    <source src="http://amssamples.streaming.mediaservices.windows.net/91492735-c523-432b-ba01-faba6c2206a2/AzureMediaServicesPromo.ism/manifest" type="application/vnd.ms-sstr+xml" />
    <p class="amp-no-js">
        To view this video please enable JavaScript, and consider upgrading to a web browser that supports HTML5 video
    </p>
</video>
```

For more details or to see how to use manual setup mode, see the [Media Player quick start documentation](http://amp.azure.net/libs/amp/latest/docs/index.html#quick-start)


## **Recommended Documents**

* [Media Player quick start documentation](http://amp.azure.net/libs/amp/latest/docs/index.html#quick-start)<br>
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)


