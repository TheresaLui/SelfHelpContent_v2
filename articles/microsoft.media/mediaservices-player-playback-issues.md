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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Azure Media Player playback issues

## **Recommended Steps**

1. Check your error code against the known list [Azure Media Player error codes](http://amp.azure.net/libs/amp/latest/docs/index.html#error-codes)
2. Remove all content protection (AES) or DRM encryption first from the stream to rule out DRM related issues
3. Test your (non-DRM) content using the [Azure Media Services test player](https://ampdemo.azureedge.net/azuremediaplayer.html)
4. Test your (non-DRM) on target devices (iOS or Android) to confirm playback
5. Confirm that the content is encoded properly, with the correct codecs and bitrates for the target devices per the manufacturers guidance
6. Confirm that you are using the proper [player heuristics profile](http://amp.azure.net/libs/amp/latest/docs/index.html#amp.player.heuristicprofile) for your streaming scenario
7. Review the [known issues list](http://amp.azure.net/libs/amp/latest/docs/known_issues.html) for Azure Media Player

### **Error Codes and catching errors**

When playback cannot start or has stopped, an error event will be fired and the error() function will return the error code and an optional message which is to help the developer get more details.

To catch errors, add the 'error' event listener to the player:

```
var myPlayer = amp('vid1');
myPlayer.addEventListener('error', function() {
    var errorDetails = myPlayer.error();
    var code = errorDetails.code;
    var message = errorDetails.message;
}
```

For details on the player error codes and their meanings see [Azure Media Player error codes](http://amp.azure.net/libs/amp/latest/docs/index.html#error-codes).

### **What browsers and OS are supported for Media Player?**

See the [browser and OS compatibility matrix](http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix) for Azure Media Player.

### **How do I check if my browser supports Media Source Extensions?**

For modern streaming playback for work (DASH, HLS) your browser should support Media Source Extension.
See the ["Can I Use" website](https://caniuse.com/#feat=mediasource).

### **How do I check if my browser supports Encrypted Media Extensions?**

For DRM content to playback, check the support matrix for EME on the browser and confirm the proper DRM is configured for targeting that browser. See the ["Can I Use" website](https://caniuse.com/#feat=eme).

### **Does my browser or target device support HEVC/H.265 video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=hevc).

If you are looking for device support of HEVC, please check with the device manufacturer to determine which hardware releases include support for HEVC playback.  

**Apple iOS and HEVC**

For iOS devices, HEVC playback was included in iOS 11.0 or higher. iPhone X, iPhone 8/Plus, iPhone 7/6s/6/Plus. Not all phone models are capable of playing back 4K and may be limited to specific resolutions and frame rate requirements. For example, iPhone 6/Plus can play HEVC video only up to 1080p at 240fps. 
iPhone XS/XR/X, iPhone 8/Plus, iPhone 7/6s/Plus with Apples A9, A10 chipset (or later) support up to 4K 2160p playback at common frame rates. 

For details on supported Apple devices for HEVC, please search HEVC in the [Apple support system](https://support.apple.com/kb/index?page=search&q=HEVC&product=&doctype=SPECIFICATIONS&currentPage=1&includeArchived=false&locale=en_US).

**Android and HEVC**

Android supports HEVC in Android 5.0+ on certain OEM hardware. 

- Chromecast Ultra supports HEVC
- Android mobile has support for HEVC, but typically only up to Main Level 3 on mobile devices (very limited support in market). See [video formats and codecs supported by Android mobile.](https://developer.android.com/guide/topics/media/media-formats#video-codecs).
- Android TV support for HEVC up to Main Level 4.1. See [video formats and codecs supported by Android TV](https://developer.android.com/guide/topics/media/media-formats#video-codecs) for details. 

### **Does my browser support H.264/AVC video playback?**

See the ["Can I Use" website](https://caniuse.com/#feat=mpeg4).

### **Why will my video not play back on a specific Android model?**

Successful playback on Android devices requires a combination of device capabilities, graphics support, codec rendering, OS support and more. Since Android is an open source platform which allows phone manufacturers to change the base Android OS provided by Google, this caused fragmentation in the Android compatibility for video and audio playback and some devices may not be supported because of a lack in features. As well, some Android devices do not have support for all popular codecs (HEVC, AAC, H.264).

## **Recommended Documents**

* [Azure Media Player Error Codes](http://amp.azure.net/libs/amp/latest/docs/index.html#error-codes)
* [Azure Media Player overview](https://docs.microsoft.com/azure/media-services/latest/use-azure-media-player)<br>
* [Azure Media Player documentation](http://amp.azure.net/libs/amp/latest/docs/index.html)<br>
* [Azure Media Player sample streams](https://amp.azure.net/libs/amp/latest/docs/samples.html)<br>
* [Azure Media Player changelog](http://amp.azure.net/libs/amp/latest/docs/changelog.html)
