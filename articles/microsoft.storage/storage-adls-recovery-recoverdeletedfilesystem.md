<properties
	pageTitle="Azure Data Lake Gen 2 storage deletion and recovery"
	description="Azure Data Lake Gen 2 storage recover deleted file system"
	infoBubbleText=""
	service="microsoft.storage"
	resource="datalakestoragegen2"
	authors="ramMSFT"
	ms.author="raprasad"
	displayOrder=""
	articleId="21148a81-886b-41fa-92eb-dcf0bdda35e8"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32612607"
	resourceTags=""
	productPesIds="16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_DataLakeStorageGen2"
/>

# Azure Data Lake Gen2 Storage recover deleted file system

## **Recommended Steps**

File system recovery is only possible under the following conditions. Please check if:

1. File system was deleted in the last 14 days
2. Storage Account replication is configured as [Geo-redundant storage(GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs) or [Read-access-geo-redundant storage(RA-GRS)](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage)<br>
3. A new File system with the same name has not been created since

**Note:** Garbage collection could occur on our system at any time, so we cannot guarantee successful recovery.

## **Recommended Documents**

* [File system - Delete](https://docs.microsoft.com/rest/api/storageservices/datalakestoragegen2/filesystem/delete)<br>
* [Access control in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control/)<br>
