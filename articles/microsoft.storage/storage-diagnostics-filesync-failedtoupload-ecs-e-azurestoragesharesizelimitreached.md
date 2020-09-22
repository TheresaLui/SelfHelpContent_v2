<properties
pageTitle="Sync failed to upload - ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED"
description="Sync failed to upload - ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED"
diagnosticScenario="Sync failed to upload - ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_AZURE_STORAGE_SHARE_SIZE_LIMIT_REACHED**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8603e or -2134351810**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>The file cannot be synced because the Azure file share limit is reached.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
1. Navigate to the sync group within the Storage Sync Service
2. Select the cloud endpoint within the sync group
3. Note the Azure file share name in the opened pane
4. Select the linked storage account. If this link fails, the referenced storage account has been removed
5. Select **Files** to view the list of file shares
6. Click the three dots at the end of the row for the Azure file share referenced by the cloud endpoint
7. Verify that the **Usage** is below the **Quota**. Note unless an alternate quota has been specified, the quota will match the [maximum size of the Azure file share](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets)

If the share is full and a quota is not set, one possible way of fixing this issue is to make each subfolder of the current server endpoint into its own server endpoint in their own separate sync groups. This way each subfolder will sync to individual Azure file shares.

## **Recommended Documents**
- [Current limits for an Azure file share](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets)
- [Maximum size of the Azure file share](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


