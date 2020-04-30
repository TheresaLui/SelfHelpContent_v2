<properties
pageTitle="Sync failed to upload - ERROR_ALREADY_EXISTS"
description="Sync failed to upload - ERROR_ALREADY_EXISTS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ERROR_ALREADY_EXISTS"
diagnosticScenario="Sync failed to upload - ERROR_ALREADY_EXISTS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ERROR_ALREADY_EXISTS**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**  due to **error code: 0x800700B7 or -2147024713**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the item already exists in the destination and sync is not aware of the change.
<!--/issueDescription-->


## **Recommended Steps**
No action required. Sync will stop logging this error once change detection runs on the destination and sync is aware of this new item.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
