<properties
	pageTitle="How to check if qualifies for recovery attempt"
	description="How to check if qualifies for recovery attempt"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="1f1abe1a-a5ed-4a98-b5e2-72bb79912ce6"
/>

# How to check if qualifies for recovery attempt

Please note that it is impossible to recover Data at the blob level. To prevent this, you can leverage on Backup and archive solutions in Azure, enabling Azure Soft Delete for Blobs or Azure Blob Snapshots.

1. To avoid this to happen in the future the most recommended feature to use is Soft Delete: [Storage Blob Soft Delete](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-soft-delete)
2. We can also recommend Snapshot feature: [Blob Snapshot](https://docs.microsoft.com/en-us/rest/api/storageservices/Creating-a-Snapshot-of-a-Blob)
3. Here are two sample codes on the feature:
 	1. [Storage Blob Snapshots](https://docs.microsoft.com/en-us/azure/storage/storage-blob-snapshots)
 	2. [Storage blob snapshots with powershell](https://blogs.msdn.microsoft.com/cie/2016/05/17/using-blob-snapshots-with-powershell/)

NOTE : Depending on circumstances, only partial data may be recoverable. Individual entities are NOT recoverable. Recovery is not possible if data within a queue was deleted - only if the whole queue was deleted
