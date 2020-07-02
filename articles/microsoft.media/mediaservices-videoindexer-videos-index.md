<properties
    pageTitle="Indexing Videos"
    description="Indexing Videos"
    infoBubbleText=""
	service="microsoft.media"
	resource="mediaservices"
    authors="ReutAmior"
    ms.author="t-reutam"
    displayOrder="1"
    articleId="mediaservices-videoindexer-videos-index"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32740743,32740744"
    resourceTags=""
    productPesIds="16535"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_Media_VI"
/>

# Indexing Videos

When uploading videos with Video Indexer API, you have the following upload options:
* Upload your video from a URL (preferred),
* Send the video file as a byte array in the request body,
* Use existing Azure Media Services asset by providing the [asset ID](https://docs.microsoft.com/azure/media-services/latest/assets-concept) (supported in paid accounts only).
Once your video has been uploaded, Video Indexer (optionally) encodes the video. When creating a Video Indexer account, you can choose a free trial account (where you get a certain number of free indexing minutes) or a paid option (where you are not limited by the quota). With free trial, Video Indexer provides up to 600 minutes of free indexing to website users and up to 2400 minutes of free indexing to API users. With paid option, you create a Video Indexer account that is [connected to your Azure subscription and an Azure Media Services account](https://docs.microsoft.com/azure/media-services/video-indexer/connect-to-azure). You pay for minutes indexed as well as the Media Account related charges.

## Uploading considerations and limitations

* A name of the video must be no greater than 80 characters.
* When uploading your video based on the URL (preferred) the endpoint must be secured with TLS 1.2 (or higher).
* The upload size with the URL option is limited to 30GB.
* The request URL length is limited to 6144 characters where the query string URL length is limited to 4096 characters .
* The upload size with the byte array option is limited to 2GB.
* The byte array option times out after 30 min.
* The URL provided in the "videoURL" parameter needs to be encoded.
* Indexing Media Services assets has the same limitation as indexing from URL.
* Video Indexer has a max duration limit of 4 hours for a single file.
* The URL needs to be accessible (for example a public URL). If it is a private URL, the access token need to be provided in the request.
* The URL has to point to a valid media file and not to a webpage, such as a link to the www.youtube.com page.
* In a paid account you can upload up to 50 movies per minute, and in a trial account up to 5 movies per minute.

## **Recommended Documents**

Learn how to upload and index your videos with these options:
* [The Video Indexer website](https://docs.microsoft.com/azure/media-services/video-indexer/upload-index-videos#website)
* [The Video Indexer APIs](https://docs.microsoft.com/azure/media-services/video-indexer/upload-index-videos#apis)