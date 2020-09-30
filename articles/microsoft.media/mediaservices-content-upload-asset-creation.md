<properties
	pageTitle="Create an Asset"
	description="Create an Asset"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-content-upload-asset-creation"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632079"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Create an Asset

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

You need to create an Asset if you want to encode or analyze your on-demand content. Or, if you have a Live Output that is associated with an Asset. A Live Output uses an Asset to store recorded videos.

## **Recommended Steps**

**Upload digital files into Assets**

The following steps describe how to upload a file and then encode or analyze the uploaded file. <br>

1. Use the Media Services v3 API to create a new "input" Asset. This operation creates a container in the storage account associated with your Media Services account. The API returns the container name, for example: `"container": "asset-b8d8b68a-2d7f-4d8c-81bb-8c7bbbe67ee4"`. If you already have a blob container that you want to associate with an Asset, you can specify the container name when creating the Asset. Media Services currently only supports blobs in the container root and not with paths in the file name. Thus, a container with the "input.mp4" file name will work. However, a container with the "videos/inputs/input.mp4" file name, will not work.

	You can use the Azure CLI to upload directly to any storage account and container that you have rights to in your subscription.
	
	The container name must be unique and follow storage naming guidelines. The name doesn't have to follow the Media Services Asset container name (Asset-GUID) formatting. `az storage blob upload -f /path/to/file -c MyContainer -n MyBlob`.<br>
	
2. Get a SAS URL with read-write permissions that will be used to upload digital files into the Asset container. You can use the Media Services API to [list the asset container URLs](https://docs.microsoft.com/rest/api/media/assets/listcontainersas).<br>
3. Use the Azure Storage APIs or SDKs (for example, the [Storage REST API](https://docs.microsoft.com/azure/storage/common/storage-rest-api-auth), [JAVA SDK](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-java-v10), or [.NET SDK](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-dotnet?tabs=windows)) to upload files into the Asset container.<br>
4. Use Media Services v3 APIs to create a Transform and a Job to process your "input" Asset. For more information, see [Transforms and Jobs](https://docs.microsoft.com/azure/media-services/latest/transforms-jobs-concept).

**Create a new asset**

REST:

```
    PUT https://management.azure.com/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Media/mediaServices/{amsAccountName}/assets/{assetName}?api-version=2018-07-01
```

Also, see the [Create an Asset with REST](https://docs.microsoft.com/rest/api/media/assets/createorupdate#examples) example. The example shows how to create the **Request Body** where you can specify useful information like description, container name, storage account, and other information.

cURL:

```
    curl -X PUT \
      'https://management.azure.com/subscriptions/00000000-0000-0000-000000000000/resourceGroups/resourceGroupName/providers/Microsoft.Media/mediaServices/amsAccountName/assets/myOutputAsset?api-version=2018-07-01' \
      -H 'Accept: application/json' \
      -H 'Content-Type: application/json' \
      -d '{
      "properties": {
        "description": "",
      }
    }'
```

.NET:

```
    Asset asset = await client.Assets.CreateOrUpdateAsync(resourceGroupName, accountName, assetName, new Asset());
```

Also, see [.NET example](https://docs.microsoft.com/azure/media-services/latest/job-input-from-local-file-how-to).

## **Recommended Documents**

* [Encoding with Media Services v3](https://docs.microsoft.com/azure/media-services/latest/encoding-concept)<br>
* [Using a cloud DVR](https://docs.microsoft.com/azure/media-services/latest/live-event-cloud-dvr)<br>
* [Tutorial: Encode a remote file based on URL and stream the video - REST](https://docs.microsoft.com/azure/media-services/latest/stream-files-tutorial-with-rest)
