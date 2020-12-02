<properties
	pageTitle="How to Recover Azure Storage Files and FileShares"
	description="How to Recover Azure Storage Files and FileShares"
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
	articleId="da25f29a-c8ef-493d-8476-6464b72f618b"
/>

# How to Recover Azure Storage Files and FileShares

Azure Storage Files and FileShares are generally not recoverable. Please check if customer has fileshare snapshots. If present they can copy data out from the share snapshot using storage explorer as follows.

**Overview of share snapshots for Azure Files**

Azure Files provides the capability to take share snapshots of file shares. Share snapshots capture the share state at that point in time. In this article, we describe what capabilities share snapshots provide and how you can take advantage of them in your custom use case.

**When to use share snapshots**

1. Protection against application error and data corruption
2. Applications that use file shares perform operations such as writing, reading, storage, transmission, and processing. If an application is misconfigured or an unintentional bug is introduced, accidental overwrite or damage can happen to a few blocks. To help protect against these scenarios, you can take a share snapshot before you deploy new application code. If a bug or application error is introduced with the new deployment, you can go back to a previous version of your data on that file share.
3. Protection against accidental deletions or unintended changes
4. Imagine that you're working on a text file in a file share. After the text file is closed, you lose the ability to undo your changes. In these cases, you then need to recover a previous version of the file. You can use share snapshots to recover previous versions of the file if it's accidentally renamed or deleted.
5. General backup purposes

After you create a file share, you can periodically create a share snapshot of the file share to use it for data backup. A share snapshot, when taken periodically, helps maintain previous versions of data that can be used for future audit requirements or disaster recovery.

**Copying data back to a share from share snapshot**

Copy operations that involve files and share snapshots follow these rules:

1. You can copy individual files in a file share snapshot over to its base share or any other location. You can restore an earlier version of a file or restore the complete file share by copying file by file from the share snapshot. The share snapshot is not promoted to base share.
2. The share snapshot remains intact after copying, but the base file share is overwritten with a copy of the data that was available in the share snapshot. All the restored files count toward "changed content."
3. You can copy a file in a share snapshot to a different destination with a different name. The resulting destination file is a writable file and not a share snapshot. In this case, your base file share will remain intact.
4. When a destination file is overwritten with a copy, any share snapshots associated with the original destination file remain intact.

**Recommended Steps Using Azure Storage explorer:**

1. Navigate to the share using storage explorer.
2. Choose View Share Snapshots from the top ribbon
3. Double click on the preferred snapshot
4. Right click on the required file and choose to Restore Snapshot.

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
3. [Quickstart: Use Azure Storage Explorer](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer)


