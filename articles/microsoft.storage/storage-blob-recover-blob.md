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
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="7e882f40-1c40-4872-ba02-8f59390d44fd"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Recover deleted Blob

## **Recommended Steps**
Blob recovery is only possible under the following conditions.  Please check if:

1.	This is a critical production data
2.	A new blob with the same name has not been re-created 
3.	Blob was deleted in the last:<br>
	a) 7 days for standard storage<br>
	b) 3 days for premium storage<br>

**Note:** As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. Recovery is a best-effort process, this blob may not be recoverable even when all conditions above are true.<br>

Enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to protect your data against accidental deletion.

## **Recommended Documents**

* [Soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)
