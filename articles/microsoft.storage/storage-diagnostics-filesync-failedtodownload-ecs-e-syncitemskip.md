<properties
pageTitle="Sync failed to download - ECS_E_SYNC_ITEM_SKIP"
description="Sync failed to download - ECS_E_SYNC_ITEM_SKIP"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDownload_ECS_E_SYNC_ITEM_SKIP"
diagnosticScenario="Sync failed to download - ECS_E_SYNC_ITEM_SKIP"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to download file(s) due to error _**ECS_E_SYNC_ITEM_SKIP**_

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80205 or -2134375931**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file was skipped but will be synced during the next sync session.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**

No action is required. The file will be synced during the next sync session.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
