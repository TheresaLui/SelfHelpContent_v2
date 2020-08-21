<properties
pageTitle="Server endpoint creation failed - ECS_E_SYNC_SHARE_DUPLICATE_PATH"
description="Server endpoint creation failed - ECS_E_SYNC_SHARE_DUPLICATE_PATH"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_SYNC_SHARE_DUPLICATE_PATH"
diagnosticScenario="Server endpoint creation failed - ECS_E_SYNC_SHARE_DUPLICATE_PATH"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint creation failed due to error ECS_E_SYNC_SHARE_DUPLICATE_PATH


<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: -2134376427 or 0x80c80015**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if another server endpoint is already syncing the server endpoint path specified. Azure File Sync does not support multiple server endpoints syncing the same directory or volume. 
<!--/issueDescription-->

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

