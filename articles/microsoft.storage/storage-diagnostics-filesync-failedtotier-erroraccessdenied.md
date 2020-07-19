<properties
pageTitle="Sync failed to tier - ERROR_ACCESS_DENIED"
description="Sync failed to tier - ERROR_ACCESS_DENIED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ERROR_ACCESS_DENIED"
diagnosticScenario="Sync failed to tier - ERROR_ACCESS_DENIED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ERROR_ACCESS_DENIED**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070005 or -2147024891**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs due to access denied error. This error can occur if the file is located on a DFS-R read-only replication folder. <br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
Azure Files Sync does not support server endpoints on DFS-R read-only replication folders. See [planning guide](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#distributed-file-system-dfs) for more information.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Planning guide](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#distributed-file-system-dfs)



