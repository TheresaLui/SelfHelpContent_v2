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
	cloudEnvironments="public, blackForest, fairfax, mooncake"
	articleId="7e882f40-1c40-4872-ba02-8f59390d44fd"
/>

# Recover deleted Blob

## **Recommended Steps**
Blob recovery is only possible under the following conditions.  Please check if:

1.  Blob was deleted in the last 14 days<br> 
2.  Storage account replication is configured as [Geo-redundant storage (GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs) or [Read-access geo-redundant storage (RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage) or [Geo-zone-redundant storage (GZRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-gzrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) because we need the geo-replicated data for recovery<br>
3. A new blob with the same name has not been created since

**Note:** As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. Recovery is a best-effort process, this blob may not be recoverable even when all conditions above are true.<br>

Enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to protect your data against accidental deletion.

## **Recommended Documents**

* [Soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)
