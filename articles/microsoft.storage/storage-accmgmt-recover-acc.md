<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="Passaree"
    ms.author="passap"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32602701,32642178,32688873"
    resourceTags="recovery"
    productPesIds="15629,16459"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="e6c363fc-ee76-4afb-8278-bbb74b17051e"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Recover deleted storage account

## **Recommended Steps**

Storage resource recovery is only possible if **a new storage object with the same name has not be re-created since** and if the following conditions are true.

**Resource group** recovery:

We can only attempt to recover deleted storage accounts within the resource group that was deleted in the last 14 days. All other resources will need to be manually rebuild.

**Storage account** recovery:

- The storage account was deleted in the last 14 days


**Container** recovery:

1. The container was deleted in the last 14 days<br> 
2. Storage account replication is configured as one of the following (we need the geo-replicated data for recovery):
   * [Geo-redundant storage (GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs)
   * [Read-access geo-redundant storage (RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage)
   * [Geo-zone-redundant storage (GZRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-gzrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) 

**Blob and disk** recovery:

1.	This is a critical production data
2.	Blob was deleted in the last:<br>
	a) 7 days for standard storage<br>
	b) 3 days for premium storage<br>

**Note:** It may **not** be possible to recover deleted data even if above conditions are true. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

## **Recommended Documents**

* [Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)<br>
* [Recovery of deleted storage account](https://docs.microsoft.com/azure/storage/files/storage-how-to-recover-deleted-account)
* [Recovery of deleted storage blob container](https://docs.microsoft.com/azure/storage/common/storage-account-container-recovery)
* [Soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)

