<properties
	pageTitle="Azure Media Player playback issues"
	description="Azure Media Player playback issues"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-player-playback-issues"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632111"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Azure Media Player playback issues

## **Recommended Steps**

1. Remove all content protection (AES) or DRM encryption first from the stream to rule out DRM related issues.
2. Test your (non-DRM) content using the [Azure Media Services test player](https://ampdemo.azureedge.net/azuremediaplayer.html)
3. Test your (non-DRM) on target devices (iOS or Android) to confirm playback. 
4. Confirm that the content is encoded properly, with the correct codecs and bitrates for the target devices per the manufacturers guidance. 
5. Confirm that you are using the proper [player heuristics profile](http://amp.azure.net/libs/amp/latest/docs/index.html#amp.player.heuristicprofile) for your streaming scenario. 
6. Review the [known issues list](http://amp.azure.net/libs/amp/latest/docs/known_issues.html) for Azure Media Player

### **What browsers and OS are supported for Media Player?**

See the [browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix) for Azure Media Player

### **How do I check if my browser supports Media Source Extensions**

For modern streaming playback for work (DASH, HLS) your browser should support Media Source Extension.
See the ["Can I Use" website - https://caniuse.com/#feat=mediasource](https://caniuse.com/#feat=mediasource)

### **How do I check if my browser supports Encrypted Media Extensions**

For DRM content to playback, check the support matrix for EME on the browser and confirm the proper DRM is configured for targeting that browser. 
See the ["Can I Use" website - https://caniuse.com/#feat=eme](https://caniuse.com/#feat=eme)

### **Does my browser support HEVC/H.265 video playback**

See the ["Can I Use" website - https://caniuse.com/#feat=hevc](https://caniuse.com/#feat=hevc)

### **Does my browser support H.264/AVC video playback**

See the ["Can I Use" website - https://caniuse.com/#feat=mpeg4](https://caniuse.com/#feat=mpeg4)

### **Why will my video not play back on a specific Android model?**

Successful playback on Android devices requires a combination of device capabilities, graphics support, codec rendering, OS support and more. Since Android is an open source platform which allows phone manufacturers to change the base Android OS provided by Google, this caused fragmentation in the Android compatibility for video and audio playback and some devices may not be supported because of a lack in features. 
Also, some Android devices do not have support for all popular codecs (HEVC, AAC, H.264).

## **Recommended Documents**

* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)<br>



