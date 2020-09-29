<properties
pageTitle="Sync failed error - SYNC_BLOCKED_ON_CHANGE_DETECTION_POST_RESTORE"
description="Sync failed error - user request throttled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_SYNC_BLOCKED_ON_CHANGE_DETECTION_POST_RESTORE"
diagnosticScenario="Sync failed error - SYNC_BLOCKED_ON_CHANGE_DETECTION_POST_RESTORE"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - SYNC_BLOCKED_ON_CHANGE_DETECTION_POST_RESTORE
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83075 or -2134364043**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/> This error occurs when a file or file share (cloud endpoint) is restored using Azure Backup, sync is blocked until change detection completes on the Azure file share. Change detection runs immediately once the restore is complete and the duration is based on the number of files in the file share.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action is required. Sync will resume once change detection completes.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
