<properties
pageTitle="Sync failed error - SYNC_E_METADATA_INVALID_OPERATION"
description="Sync failed error - SYNC_E_METADATA_INVALID_OPERATION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_SYNC_E_METADATA_INVALID_OPERATION"
diagnosticScenario="Sync failed error - SYNC_E_METADATA_INVALID_OPERATION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - SYNC_E_METADATA_INVALID_OPERATION
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code 0x80041295 or -2147216747**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error typically occurs when a backup application creates a VSS snapshot and the sync database is unloaded.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action is required. If this error persists for longer than a day, create a support request.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
