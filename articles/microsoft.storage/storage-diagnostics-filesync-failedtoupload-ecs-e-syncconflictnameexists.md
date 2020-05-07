<properties
pageTitle="Sync failed to upload - ECS_E_SYNC_CONFLICT_NAME_EXISTS"
description="Sync failed to upload - ECS_E_SYNC_CONFLICT_NAME_EXISTS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_SYNC_CONFLICT_NAME_EXISTS"
diagnosticScenario="Sync failed to upload - ECS_E_SYNC_CONFLICT_NAME_EXISTS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_SYNC_CONFLICT_NAME_EXISTS**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80200 or -2134375936**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the maximum number of conflict files has been reached.Azure File Sync supports 100 conflict files per file.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, reduce the number of conflict files. The file will sync once the number of conflict files is less than 100.



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
