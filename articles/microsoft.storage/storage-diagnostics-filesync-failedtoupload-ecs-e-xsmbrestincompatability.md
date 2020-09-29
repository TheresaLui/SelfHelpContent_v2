<properties
pageTitle="Sync failed to download - ECS_E_XSMB_REST_INCOMPATIBILITY"
description="Sync failed to download - ECS_E_XSMB_REST_INCOMPATIBILITY"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDownload_ECS_E_XSMB_REST_INCOMPATIBILITY"
diagnosticScenario="Sync failed to download - ECS_E_XSMB_REST_INCOMPATIBILITY"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to download file(s) due to error _**ECS_E_XSMB_REST_INCOMPATIBILITY**_

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**  due to **error code: 0x80c80255 or -2134375851**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file or directory name contains invalid characters. For these files to sync, the files with unsupported characters must be renamed.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, see the [Unsupported Characters](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#handling-unsupported-characters) section in the Troubleshooting guide for details on handling unsupported characters and how to identify the files.

## **Recommended Documents**
- [Unsupported Characters](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#handling-unsupported-characters)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
