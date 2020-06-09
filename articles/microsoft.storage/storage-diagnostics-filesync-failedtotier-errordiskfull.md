<properties
pageTitle="Sync failed to tier - ERROR_DISK_FULL"
description="Sync failed to tier - ERROR_DISK_FULL"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ERROR_DISK_FULL"
diagnosticScenario="Sync failed to tier - ERROR_DISK_FULL"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ERROR_DISK_FULL**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070070 or -2147024784**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to insufficient disk space on the volume where the server endpoint is located. <br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, free at least 100 MB of disk space on the volume where the server endpoint is located.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



