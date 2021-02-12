<properties
pageTitle="Sync failed to upload - ECS_E_SYNC_CONSTRAINT_CONFLICT_SESSION_FAILED"
description="Sync failed to upload - ECS_E_SYNC_CONSTRAINT_CONFLICT_SESSION_FAILED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_SYNC_CONSTRAINT_CONFLICT_SESSION_FAILED"
diagnosticScenario="Sync failed to upload - ECS_E_SYNC_CONSTRAINT_CONFLICT_SESSION_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_SYNC_CONSTRAINT_CONFLICT_SESSION_FAILED**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80284 or -2134375804**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file or directory change cannot be synced yet because a dependent folder is not yet synced.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
No action is required. This item will sync after the dependent changes are synced.If the error persists, investigate the sync session failure.

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

