<properties
	pageTitle="Upload to storage"
	description="Upload to storage"
	service="microsoft.media"
	resource="mediaservices"
	authors="juliako"
	ms.author="juliako"
	displayOrder="1"
	articleId="mediaservices-content-upload-to-storage"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32632127"
	resourceTags=""
	productPesIds="14885"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Media"
/>

# Upload to storage

**NOTE:** This topic references Media Services v3 API documentation. v3 is the latest Media Services version.

To start managing content, you need to create a Media Services account and associate it with an Azure Storage account. To upload your digital files, you need to create an Asset which is used to store the content in the associated Azure blob storage container. In Media Services v3, the Storage APIs are used to upload files into Assets. In Media Services v3, you use the Azure Storage APIs or SDKs to upload files into the Asset container. 

## **Recommended Steps**

The following general steps describe how to upload a file.<br>

1. Use the Media Services v3 API to create a new "input" Asset. This operation creates a container in the storage account associated with your Media Services account. The API returns the container name, for example: `"container": "asset-b8d8b68a-2d7f-4d8c-81bb-8c7bbbe67ee4"`. If you already have a blob container that you want to associate with an Asset, you can specify the container name when creating the Asset. Media Services currently only supports blobs in the container root and not with paths in the file name. Thus, a container with the "input.mp4" file name will work. However, a container with the "videos/inputs/input.mp4" file name, will not work. 

	You can use the Azure CLI to upload directly to any storage account and container that you have rights to in your subscription. 

	The container name must be unique and follow storage naming guidelines. The name doesn't have to follow the Media Services Asset container name (Asset-GUID) formatting. `az storage blob upload -f /path/to/file -c MyContainer -n MyBlob`.<br>

2. Get a SAS URL with read-write permissions that will be used to upload digital files into the Asset container. You can use the Media Services API to [list the asset container URLs](https://docs.microsoft.com/rest/api/media/assets/listcontainersas).<br>

3. Use the Azure Storage APIs or SDKs (for example, the [Storage REST API](https://docs.microsoft.com/azure/storage/common/storage-rest-api-auth), [JAVA SDK](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-java-v10), or [.NET SDK](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-dotnet?tabs=windows)) to upload files into the Asset container

## **Recommended Documents**

* [Cloud upload and storage](https://docs.microsoft.com/azure/media-services/latest/storage-account-concept)<br>
* [Assets](https://docs.microsoft.com/azure/media-services/latest/assets-concept)<br>
* [Upload files into a Media Services account using .NET](https://docs.microsoft.com/azure/media-services/latest/job-input-from-local-file-how-to)<br>
* [Upload files into a Media Services account using REST](https://docs.microsoft.com/azure/media-services/latest/upload-files-rest-how-to)
