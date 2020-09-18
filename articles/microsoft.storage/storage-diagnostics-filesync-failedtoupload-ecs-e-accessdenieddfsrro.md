<properties
pageTitle="Sync failed to upload - ECS_E_ACCESS_DENIED_DFSRRO"
description="Sync failed to upload - ECS_E_ACCESS_DENIED_DFSRRO"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_ACCESS_DENIED_DFSRRO"
diagnosticScenario="Sync failed to upload - ECS_E_ACCESS_DENIED_DFSRRO"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_ACCESS_DENIED_DFSRRO**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80283 or -2160591491**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file is located on a DFS-R read-only replication folder.<br/><br/>Azure Files Sync does not support server endpoints on DFS-R read-only replication folders.
<!--/issueDescription-->


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Planning guide](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#distributed-file-system-dfs)
