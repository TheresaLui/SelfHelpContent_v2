<properties
pageTitle="Server endpoint creation failed - ERROR_FILE_NOT_FOUND"
description="Server endpoint creation failed - ERROR_FILE_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ERROR_FILE_NOT_FOUND"
diagnosticScenario="Sync failed to create server endpoint - ERROR_FILE_NOT_FOUND"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint - ERROR_FILE_NOT_FOUND

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code -2147024894 or 0x80070002**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the server endpoint path specified is not valid. 
<!--/issueDescription-->

## **Recommended Steps**
 Verify the server endpoint path specified is a locally attached NTFS volume. Note: Azure File Sync does not support mapped drives as a server endpoint path.
 
## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
