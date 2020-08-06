<properties
pageTitle="Server endpoint creation failed - ECS_E_GHOSTING_NOT_SUPPORTED"
description="Server endpoint creation failed - ECS_E_GHOSTING_NOT_SUPPORTED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_GHOSTING_NOT_SUPPORTED"
diagnosticScenario="Server endpoint creation failed - ECS_E_GHOSTING_NOT_SUPPORTED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint creation failed due to error ECS_E_GHOSTING_NOT_SUPPORTED

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: -2134375898 or 0x80c80226**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the server endpoint path is on the system volume and cloud tiering is enabled. Cloud tiering is not supported on the system volume. 
<!--/issueDescription-->

## **Recommended Steps**

To create a server endpoint on the system volume, disable cloud tiering when creating the server endpoint.

## **Recommended Documents**
 - [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
