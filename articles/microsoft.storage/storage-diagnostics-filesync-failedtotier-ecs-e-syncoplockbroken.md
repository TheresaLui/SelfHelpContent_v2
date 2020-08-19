<properties
pageTitle="Sync failed to tier - ECS_E_SYNC_OPLOCK_BROKEN"
description="Sync failed to tier - ECS_E_SYNC_OPLOCK_BROKEN"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_SYNC_OPLOCK_BROKEN"
diagnosticScenario="Sync failed to tier - ECS_E_SYNC_OPLOCK_BROKEN"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ECS_E_SYNC_OPLOCK_BROKEN**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80017 or -2134376425**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the file has been modified.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action required. The file will tier once the modified file has synced to the Azure file share.



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



