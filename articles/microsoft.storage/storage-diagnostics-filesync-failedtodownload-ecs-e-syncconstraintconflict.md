<properties
pageTitle="Sync failed to download - ECS_E_SYNC_CONSTRAINT_CONFLICT"
description="Sync failed to download - ECS_E_SYNC_CONSTRAINT_CONFLICT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDownload_ECS_E_SYNC_CONSTRAINT_CONFLICT"
diagnosticScenario="Sync failed to download - ECS_E_SYNC_CONSTRAINT_CONFLICT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_SYNC_CONSTRAINT_CONFLICT**_

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**  due to **error code: 0x80c80207 or -2134375929**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file or directory change cannot be synced yet because a dependent folder is not yet synced.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**

No action is required.This item will sync after the dependent changes are synced.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



