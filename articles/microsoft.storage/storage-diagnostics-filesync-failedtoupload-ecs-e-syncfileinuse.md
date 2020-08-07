<properties
pageTitle="Sync failed to upload - ECS_E_SYNC_FILE_IN_USE"
description="Sync failed to upload - ECS_E_SYNC_FILE_IN_USE"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_SYNC_FILE_IN_USE"
diagnosticScenario="Sync failed to upload - ECS_E_SYNC_FILE_IN_USE"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_SYNC_FILE_IN_USE**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80018 or -2134376424**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file has an open handle.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
No action is required. The file will sync once all open handles are closed. Also, Azure File Sync creates a temporary VSS snapshot once a day on the server to sync files that have open handles. 

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



