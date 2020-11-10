<properties
pageTitle="Sync failed to tier - ECS_E_GHOSTING_FILE_NOT_SYNCED"
description="Sync failed to tier - ECS_E_GHOSTING_FILE_NOT_SYNCED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_GHOSTING_FILE_NOT_SYNCED"
diagnosticScenario="Sync failed to tier - ECS_E_GHOSTING_FILE_NOT_SYNCED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ECS_E_GHOSTING_FILE_NOT_SYNCED**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80264 or -2134375836**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the file has not synced to the Azure file share.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action required. The file will tier once it has synced to the Azure file share.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



