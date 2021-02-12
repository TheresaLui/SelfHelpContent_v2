<properties
pageTitle="Sync failed to upload - ERROR_PATH_NOT_FOUND"
description="Sync failed to upload - ERROR_PATH_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ERROR_PATH_NOT_FOUND"
diagnosticScenario="Sync failed to upload - ERROR_PATH_NOT_FOUND"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ERROR_PATH_NOT_FOUND**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070003 or -2147942403**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the item was already deleted in the destination and sync is not aware of the change.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
No action is required.Sync will stop logging this error once change detection runs on the destination and sync detects the item was deleted.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
