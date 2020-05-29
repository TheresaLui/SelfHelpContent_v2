<properties
	pageTitle="Camera connection issue or error"
	description="Camera connection issue or error"
	service="microsoft.media"
	resource="mediaservices"
	authors="akucer"
	ms.author="akucer"
	displayOrder="1"
	articleId="mediaservices-lva-camera-connection-issue-error"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32740853"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>
# Camera connection issue or error
## **Recommended Documents**
## Supported IP cameras
Any [IP camera](https://en.wikipedia.org/wiki/IP_camera) with support for RTSP over HTTP can be used. You can search for IP cameras with RTSP support on the [ONVIF conformant](https://www.onvif.org/conformant-products/) products page by looking for devices that conform with profiles G, S, or T.

## IP Camera ingest and RTSP settings

* Do I need to use a special SDK on my device to send in a video stream?
    * No, only the RTSP protocol is supported.
* Can I also use RTMP or Smooth ingest like a Media Services Live Event?
    * No, only the RTSP protocol is supported for capturing video from IP cameras.
* Can I connect to a secure RTSP camera source?
    * No, you can only connect to a basic password authenticated camera, or open authentication RTSP camera source. When connecting to an RTSP source, you must fill out the credentials section of the media graph RTSP source.
* Can I reset or update the RTSP source URL on a graph instance?
    * Yes, when the graph instance is in the inactive state.
* Is there a simulated RTSP camera signal available to use during testing and development?
    * Yes, there is an [RTSP simulator edge module](https://docs.microsoft.com/azure/media-services/live-video-analytics-edge/get-started-detect-motion-emit-events-quickstart#deploy-modules-on-your-edge-device) available for use in the quick starts and tutorials to support the learning process. This module is provided as best-effort and may not always be available. It is strongly encouraged not to use this for more than a few hours, and you should invest in testing with an IP Camera before making plans for a production deployment.
* Do you support ONVIF discovery of IP cameras at the edge?
    * No, there is no support for ONVIF discovery of devices on the edge.
