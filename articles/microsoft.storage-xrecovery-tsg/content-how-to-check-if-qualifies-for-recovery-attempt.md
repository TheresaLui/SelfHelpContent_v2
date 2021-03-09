<properties
	pageTitle="How to check if qualifies for recovery attempt"
	description="How to check if qualifies for recovery attempt"
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
	articleId="1f1abe1a-a5ed-4a98-b5e2-72bb79912ce6"
/>

# How to check if qualifies for recovery attempt

Please note that recovering data at the blob level is best effort attempt and is not always guaranteed. To prevent this, you can leverage on Backup and archive solutions in Azure, enabling Azure Soft Delete for Blobs or Azure Blob Snapshots.

1. To avoid this to happen in the future the most recommended feature to use is Soft Delete: [Storage Blob Soft Delete](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-soft-delete)
2. We can also recommend Snapshot feature: [Blob Snapshot](https://docs.microsoft.com/en-us/rest/api/storageservices/Creating-a-Snapshot-of-a-Blob)
3. Here are two sample codes on the feature:
 	1. [Storage Blob Snapshots](https://docs.microsoft.com/en-us/azure/storage/storage-blob-snapshots)
 	2. [Storage blob snapshots with powershell](https://blogs.msdn.microsoft.com/cie/2016/05/17/using-blob-snapshots-with-powershell/)

NOTE : Depending on circumstances, only partial data may be recoverable. Individual entities are NOT recoverable. Recovery is not possible if data within a queue was deleted - only if the whole queue was deleted

<br>

# Disk Recovery #


When customers request for **Disk recovery** (be it managed or unmanaged), please collect a detailed business justification and email <cssstorageta@microsoft.com> and CC <xsupportpm@microsoft.com> with an ICM number and route the ICM to XStore/Table Server team. If you don't have access to create an ICM with XStore/Table Server team, engage one of the storage TAs or email cssstorageta@microsoft.com to route the ICM. <br>

 Before we engage PG through ICM, make sure that the following statements are true.

```
1. Business justification to show that data to recover is production data (not test data)
2. A new blob with the same name has not been created 
3. Deleted less than a week for standard 
4. Deleted less than 3 days for XIO(Premium) 
5. Disk URI (full path) 
6. Delete Time 
7. Prioritized list 