<properties
	pageTitle="How to check if storage account type qualifies for recovery attempt from ASC"
	description="How to check if storage account type qualifies for recovery attempt from ASC"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="a8c39676-02e4-47d7-9a02-9973d4c7738f"
/>

# How to check if storage account type qualifies for recovery attempt from ASC

Please note that it is impossible to recover Data at the blob level. To prevent this, you can leverage on Backup and archive solutions in Azure, enabling Azure Soft Delete for Blobs or Azure Blob Snapshots.

1. To avoid this to happen in the future the most recommended feature to use is Soft Delete: [Storage Blob Soft Delete](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-soft-delete)
2. We can also recommend Snapshot feature: [Blob Snapshot](https://docs.microsoft.com/en-us/rest/api/storageservices/Creating-a-Snapshot-of-a-Blob)
3. Here are two sample codes on the feature:
 	1. [Storage Blob Snapshots](https://docs.microsoft.com/en-us/azure/storage/storage-blob-snapshots)
 	2. [Storage blob snapshots with powershell](https://blogs.msdn.microsoft.com/cie/2016/05/17/using-blob-snapshots-with-powershell/)

NOTE : Depending on circumstances, only partial data may be recoverable. Individual entities are NOT recoverable. Recovery is not possible if data within a queue was deleted - only if the whole queue was deleted

**Checking recovery in ASC**

1. Navigate to Resource Explorer and search for the affected Storage Account resource.
2. In the Properties section, check the Type and ensure it is one of the following. No data recovery is possible for the types that do not qualify.
    1. Standard_GRS
	2. Standard_RAGRS
	3. Standard_GZRS
	4. Standard_RAGZRS

Note: As part of our data privacy guarantee, we ensure that data deleted by our customer is eventually overwritten. This storage account and all its content may not be recoverable by Azure even when all conditions above are true.
 
## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
