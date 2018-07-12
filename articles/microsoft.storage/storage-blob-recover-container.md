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
Container recovery is only possible on Containers deleted less than 14 days ago and the Storage Account replication is configured as [Geo-redundant storage (GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs) or [Read-access geo-redundant storage (RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage)<br>

We request that you do not attempt to recreate a new Container with the same name while we are attempting to recover. Garbage collection could occur on our system at anytime so there is no guarantee for recovery to be successful.

## **Recommended documents**
[Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)

