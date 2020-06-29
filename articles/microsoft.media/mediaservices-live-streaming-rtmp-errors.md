<properties
	pageTitle="Live streaming and RTMP error"
	description="Live streaming and RTMP error"
	infoBubbleText=""
	service="microsoft.media"
	resource="liveevent"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-live-streaming-rtmp-errors"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632120"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Live streaming and RTMP error

When streaming via RTMP, check firewall and/or proxy settings to confirm that outbound TCP ports 1935 and 1936 are open.

**On-premises live encoders that output RTMP**

Media Services recommends using one of following live encoders that have RTMP as output. The supported URL schemes are *rtmp://* or *rtmps://*.

**NOTE:** When streaming via RTMP, check firewall and/or proxy settings to confirm that outbound TCP ports 1935 and 1936 are open.<br/>
 When streaming via RTMPS, check firewall and/or proxy settings to confirm that outbound TCP ports 2935 and 2936 are open.

- Adobe Flash Media Live Encoder 3.2
- Haivision KB
- Haivision Makito X HEVC
- OBS Studio
- Switcher Studio (iOS)
- Telestream Wirecast 8.1+
- Telestream Wirecast S
- Teradek Slice 756
- TriCaster 8000
- Tricaster Mini HD-4
- VMIX
- xStream

**Media Services v3 (latest)**

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

[Live Events](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept) are responsible for ingesting and processing the live video feeds. When you create a Live Event, an input endpoint is created that you can use to send a live signal from a remote encoder. The remote live encoder sends the contribution feed to that input endpoint using either the [RTMP](https://www.adobe.com/devnet/rtmp.html) or [Smooth Streaming](https://msdn.microsoft.com/library/ff469518.aspx) (fragmented-MP4) protocol. For the RTMP ingest protocol, the supported URL schemes are *rtmp://* or *rtmps://*. 

Live Event ingest URLs:

In Media Services v3, [Live Events](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept) are responsible for ingesting and processing the live video feeds. Once the Live Event is created, you can get ingest URLs that you will provide to the live on-premises encoder. The live encoder uses these URLs to input a live stream. For more information, see Recommended on-premises live encoders. You can either use non-vanity URLs or vanity URLs.

Non-vanity URL is the default mode in AMS v3. You potentially get the Live Event quickly but ingest URL is known only when the live event is started. The URL will change if you do stop/start the Live Event. 
Non-Vanity is useful in scenarios when an end user wants to stream using an app where the app wants to get a live event ASAP and having a dynamic ingest URL is not a problem.

Vanity mode is preferred by large media broadcasters who use hardware broadcast encoders and don't want to re-configure their encoders when they start the Live Event. They want a predictive ingest URL, which does not change over time. <br> **NOTE:**For an ingest URL to be predictive, you need to use "vanity" mode and pass your own access token (to avoid a random token in the URL).

Live ingest URL naming rules:

The *random* string below is a 128-bit hex number (which is composed of 32 characters of 0-9 a-f).<br/>
The *access token* below is what you need to specify for fixed URL. It is also 128 bit hex number.

Non-vanity RTMP URL:

* `rtmp://<random 128bit hex string>.channel.media.azure.net:1935/<access token>`
* `rtmp://<random 128bit hex string>.channel.media.azure.net:1936/<access token>`
* `rtmps://<random 128bit hex string>.channel.media.azure.net:2935/<access token>`
* `rtmps://<random 128bit hex string>.channel.media.azure.net:2936/<access token>`

Vanity RTMP URL

* `rtmp://<live event name>-<ams account name>-<region abbrev name>.channel.media.azure.net:1935/<access token>`
* `rtmp://<live event name>-<ams account name>-<region abbrev name>.channel.media.azure.net:1936/<access token>`
* `rtmps://<live event name>-<ams account name>-<region abbrev name>.channel.media.azure.net:2935/<access token>`
* `rtmps://<live event name>-<ams account name>-<region abbrev name>.channel.media.azure.net:2936/<access token>`

**Media Services v2 (legacy)**

In Media Services v2, [Channels](https://docs.microsoft.com/azure/media-services/previous/media-services-manage-channels-overview) are responsible for ingesting and processing the live video feeds.

## **Recommended Documents**

* [Live Events](https://docs.microsoft.com/azure/media-services/latest/live-events-outputs-concept)
