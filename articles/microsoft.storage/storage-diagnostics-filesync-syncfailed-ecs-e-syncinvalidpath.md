<properties
pageTitle="Sync failed error - ECS_E_SYNC_INVALID_PATH "
description="Sync failed error - ECS_E_SYNC_INVALID_PATH"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_SYNC_INVALID_PATH"
diagnosticScenario="Sync failed error - ECS_E_SYNC_INVALID_PATH"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_SYNC_INVALID_PATH
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80019 or -2134376423**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the server endpoint path is not a local NTFS volume.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To resolve this issue, verify the path exists, is on a local NTFS volume, and is not a reparse point or existing server endpoint.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
