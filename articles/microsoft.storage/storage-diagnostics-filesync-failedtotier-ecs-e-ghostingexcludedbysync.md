<properties
pageTitle="Sync failed to tier - ECS_E_GHOSTING_EXCLUDED_BY_SYNC"
description="Sync failed to tier - ECS_E_GHOSTING_EXCLUDED_BY_SYNC"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_GHOSTING_EXCLUDED_BY_SYNC"
diagnosticScenario="Sync failed to tier - ECS_E_GHOSTING_EXCLUDED_BY_SYNC"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ECS_E_GHOSTING_EXCLUDED_BY_SYNC**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80241 or -2134375871**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file is excluded by sync.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action required. Files in the sync exclusion list cannot be tiered.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



