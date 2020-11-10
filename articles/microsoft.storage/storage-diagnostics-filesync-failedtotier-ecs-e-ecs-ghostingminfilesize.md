<properties
pageTitle="Sync failed to tier - ECS_E_GHOSTING_MIN_FILE_SIZE"
description="Sync failed to tier - ECS_E_GHOSTING_MIN_FILE_SIZE"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_GHOSTING_MIN_FILE_SIZE"
diagnosticScenario="Sync failed to tier - ECS_E_GHOSTING_MIN_FILE_SIZE"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ECS_E_GHOSTING_MIN_FILE_SIZE**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80261 or -2134375839.** This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the file size is less than the supported size.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
If the agent version is less than 9.0, the minimum supported file size is 64kb. If agent version is 9.0 and newer, the minimum supported file size is based on the file system cluster size (double file system cluster size).



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



