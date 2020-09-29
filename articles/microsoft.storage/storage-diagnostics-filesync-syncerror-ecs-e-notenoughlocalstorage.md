<properties
pageTitle="Sync error - ECS_E_NOT_ENOUGH_LOCAL_STORAGE"
description="Sync error - ECS_E_NOT_ENOUGH_LOCAL_STORAGE"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_ECS_E_NOT_ENOUGH_LOCAL_STORAGE"
diagnosticScenario="Sync error - ECS_E_NOT_ENOUGH_LOCAL_STORAGE"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# **File Sync failed with error - ECS_E_NOT_ENOUGH_LOCAL_STORAGE**

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8031a or -2134375654**. This error occurred between ***<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the file cannot be synced due to insufficient disk space on the volume.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, free up space on the volume by moving files to a different volume, or increasing the size of the volume the server endpoint is on.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
