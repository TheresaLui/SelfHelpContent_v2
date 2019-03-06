<properties
	pageTitle="Recover deleted Blob"
	description="Recover deleted Blob Troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608638"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public,MoonCake"
	articleId="7e882f40-1c40-4872-ba02-8f59390d44fd"
/>

# Recover deleted Blob
## **Recommended steps**

We sincerely apologize that we are unable to recover deleted blob without [soft delete](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) enabled.<br>

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This blob and all its content was cleaned up after deletion and is no longer recoverable by Azure.

Azure Storage now offers soft delete for blob objects so that you can more easily recover your data when it is erroneously deleted by an application or other storage account user. You can enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted blobs will be recoverable in the future. 

