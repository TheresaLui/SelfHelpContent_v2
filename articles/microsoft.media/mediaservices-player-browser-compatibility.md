<properties
	pageTitle="Azure Media Player browser and OS compatibility"
	description="Azure Media Player browser and OS compatibility"
	infoBubbleText=""
	service="microsoft.media"
	resource=""
	authors="johndeu"
	ms.author="johndeu"
	displayOrder="1"
	articleId="mediaservices-player-browser-compatibility"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632081"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public"
/>

# Azure Media Player browser and OS compatibility


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

* [Browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix)<br> 
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)


