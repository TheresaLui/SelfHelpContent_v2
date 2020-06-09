<properties
	pageTitle="Streaming endpoints"
	description="Streaming endpoints"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-stream-files-streaming-endpoints"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632122"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Streaming endpoint 

A common Media Services scenario is to encode your content and stream files using different streaming formats and content protection formats to a variety of client technologies (for example, iOS and XBOX).

[Streaming Endpoints](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept) is the dynamic packaging and streaming service in Media Services used to deliver media content to client players or to a Content Delivery Network (CDN) for further distribution. Dynamic Packaging is a feature that comes standard on all Streaming Endpoints (Standard or Premium). 

To take advantage of Dynamic Packaging, you need to have an Asset with a set of adaptive bitrate MP4 files and streaming configuration files needed by Media Services Dynamic Packaging. One way to get the files is to encode your mezzanine (source) file with Media Services. The encoding job will produce an output Asset.

To make videos in the output Asset available to clients for playback, you have to create a Streaming Locator and build streaming URLs. When creating the Streaming Locator, in addition to the Asset's name, you need to specify a Streaming Policy. Streaming Policies enable you to define streaming protocols and encryption options (if any) for your Streaming Locators. 

Based on the specified format in the streaming client manifest (HLS, DASH, or Smooth), your clients can receive the stream in the chosen protocol.

### Delivery Protocols

|Protocol|Example|
|---|---|
|HLS V4	|`https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest(format=m3u8-aapl)`|
|HLS V3	|`https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest(format=m3u8-aapl-v3)`|
|HLS CMAF| `https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest(format=m3u8-cmaf)`|
|MPEG DASH CSF| `https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest(format=mpd-time-csf)` |
|MPEG DASH CMAF|`https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest(format=mpd-time-cmaf)` |
|Smooth Streaming| `https://amsv3account-usw22.streaming.media.azure.net/21b17732-0112-4d76-b526-763dcd843449/ignite.ism/manifest`|

**NOTE**: Currently, you cannot use the Azure portal to manage v3 resources. Use the [REST API](https://aka.ms/ams-v3-rest-ref), [CLI](https://aka.ms/ams-v3-cli-ref), or one of the supported [SDKs](https://docs.microsoft.com/azure/media-services/latest/developers-guide).

## **Recommended Documents** 

* [Streaming Endpoints](https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept)<br>
* [Dynamic packaging](https://docs.microsoft.com/azure/media-services/latest/dynamic-packaging-overview)<br>
* [Tutorial: Encode a remote file based on URL and stream the video - REST](https://docs.microsoft.com/azure/media-services/latest/stream-files-tutorial-with-rest)<br>
* [Tutorial: Upload, encode, and stream videos using .NET](https://docs.microsoft.com/azure/media-services/latest/stream-files-tutorial-with-api)<br>
* [Download the results from the specified output asset](https://github.com/Azure-Samples/media-services-v3-dotnet-tutorials/blob/master/AMSV3Tutorials/UploadEncodeAndStreamFiles/Program.cs#L464)
