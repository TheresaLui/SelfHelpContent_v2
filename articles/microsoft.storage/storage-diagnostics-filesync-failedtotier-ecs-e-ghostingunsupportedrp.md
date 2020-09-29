<properties
pageTitle="Sync failed to tier - ECS_E_GHOSTING_UNSUPPORTED_RP"
description="Sync failed to tier - ECS_E_GHOSTING_UNSUPPORTED_RP"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_GHOSTING_UNSUPPORTED_RP"
diagnosticScenario="Sync failed to tier - ECS_E_GHOSTING_UNSUPPORTED_RP"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ECS_E_GHOSTING_UNSUPPORTED_RP**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80262 or -2134375838**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because it's an unsupported reparse point.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
If the file is a Data Deduplication reparse point, follow the steps in the [planning guide](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#data-deduplication) to enable Data Deduplication support. Files with reparse points other than Data Deduplication are not supported and will not be tiered.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Planning guide](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#data-deduplication)



