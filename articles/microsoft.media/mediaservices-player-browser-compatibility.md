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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Player browser and OS compatibility


### **What browsers and OS are supported for Media Player?**

See the [browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix) for Azure Media Player.

### **How do I check if my browser supports Media Source Extensions?**

For modern streaming playback for work (DASH, HLS) your browser should support Media Source Extension. See the ["Can I Use" website](https://caniuse.com/#feat=mediasource).

### **How do I check if my browser supports Encrypted Media Extensions?**

For DRM content to playback, check the support matrix for EME on the browser and confirm the proper DRM is configured for targeting that browser. See the ["Can I Use" website](https://caniuse.com/#feat=eme).

### **Does my browser/device supports HEVC/H.265 video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=hevc).

If you are looking for device support of HEVC, please check with the device manufacturer to determine which hardware releases include support for HEVC playback.  

For iOS devices, HEVC playback was included in iOS 11.0 or higher: iPhone X, iPhone 8/Plus, iPhone 7/6s/6/Plus. Not all phone models are capable of playing back 4K and may be limited to specific resolutions and frame rate requirements. For example, iPhone 6/Plus can play HEVC video only up to 1080p at 240fps. iPhones XS/XR/X, iPhone 8/Plus, iPhone 7/6s/Plus with Apples A9, A10 chipset (or later) support up to 4K 2160p playback at common frame rates. 

Android supports HEVC in Android 5.0 or higher on certain devices. 

### **Does my browser support H.264/AVC video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=mpeg4).

### **Why will my video not play back on a specific Android model?**

Successful playback on Android devices requires a combination of device capabilities, graphics support, codec rendering, OS support, and more. Since Android is an open source platform which allows phone manufacturers to change the base Android OS provided by Google, this caused fragmentation in the Android compatibility for video and audio playback and some devices may not be supported because of a lack in features. As well, some Android devices do not have support for all popular codecs (HEVC, AAC, H.264).

## **Recommended Documents**

* [Browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix)<br> 
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)
