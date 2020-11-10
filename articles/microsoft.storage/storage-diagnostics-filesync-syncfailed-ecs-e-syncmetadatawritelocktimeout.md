<properties
pageTitle="Sync failed error - ECS_E_SYNC_METADATA_WRITE_LOCK_TIMEOUT"
description="Sync failed error - ECS_E_SYNC_METADATA_WRITE_LOCK_TIMEOUT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_SYNC_METADATA_WRITE_LOCK_TIMEOUT"
diagnosticScenario="Sync failed error - ECS_E_SYNC_METADATA_WRITE_LOCK_TIMEOUT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_SYNC_METADATA_WRITE_LOCK_TIMEOUT

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80219 or -2134375911**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error usually resolves itself, and can occur if there are:<br/>- A high number of file changes across the servers in the sync group.<br/>- A large number of errors on individual files and directories.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
No action is required. If this error persists for longer than a day, create a support request.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
