<properties
pageTitle="Sync error - ERROR_INVALID_NAME"
description="Sync error - ERROR_INVALID_NAME"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_ERROR_INVALID_NAME"
diagnosticScenario="Sync error - ERROR_INVALID_NAME"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# **File Sync failed with error - ERROR_INVALID_NAME**

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x8007007b or -2147024773**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file or directory name contains invalid characters. For these files to sync, the files with unsupported characters must be renamed.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, see the [Unsupported Characters](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#handling-unsupported-characters) section in the Troubleshooting guide for details on handling unsupported characters and how to identify the files.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Unsupported Characters](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#handling-unsupported-characters)
