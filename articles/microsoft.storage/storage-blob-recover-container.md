<properties
	pageTitle="Recover deleted Container"
	description="Recover deleted Container Troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602730"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public,MoonCake"
/>

# Recover deleted Container

## **Recommended steps**

Container recovery is only possible under the following conditions. Please check if:

1.  Container was deleted in the last 14 days<br> 
2.  Storage Account replication is configured as [Geo-redundant storage (GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs) or [Read-access geo-redundant storage (RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage)<br>
3. A new Container with the same name has not been created since

**Note:** Garbage collection could occur on our system at any time, so we cannot guarantee successful recovery.

## **Recommended documents**
[Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)

