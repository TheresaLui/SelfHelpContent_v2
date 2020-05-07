<properties
pageTitle="Server endpoint creation failed - ECS_E_SYNC_FOLDER_ORPHANED_TIERED_PATH"
description="Server endpoint creation failed - ECS_E_SYNC_FOLDER_ORPHANED_TIERED_PATH"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_SYNC_FOLDER_ORPHANED_TIERED_PATH"
diagnosticScenario="Server endpoint creation failed - ECS_E_SYNC_FOLDER_ORPHANED_TIERED_PATH"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint creation failed due to error ECS_E_SYNC_FOLDER_ORPHANED_TIERED_PATH

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code -2160590967 or 0x80c80077**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the server endpoint path contains orphaned tiered files.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, 

1. If a server endpoint was recently removed, wait until the orphaned tiered files cleanup has completed. 
2. If the error continues to occur after orphaned tiered files cleanup has completed ,remove the orphaned tiered files by performing the steps documented in the [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint).

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

