<properties
	pageTitle="Recover deleted Container"
	description="Recover deleted Container Troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602730"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
	articleId="715f7802-5471-4db4-8a72-c31c1248a015"
/>

# Recover deleted Container

## **Recommended Steps**

Container recovery is only possible under the following conditions. Please check if:

1.  Container was deleted in the last 14 days<br> 
2.  Storage account replication is configured as [Geo-redundant storage (GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs) or [Read-access geo-redundant storage (RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage) or [Geo-zone-redundant storage (GZRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-gzrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) because we need the geo-replicated data for recovery<br>
3. A new container with the same name has not been created since

**Note:** As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. Recovery is a best-effort process, this container may not be recoverable even when all conditions above are true.<br><br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

## **Recommended Documents**

* [Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)

