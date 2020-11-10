<properties
pageTitle="Sync failed to recall - ERROR_OUTOFMEMORY"
description="Sync failed to recall - ERROR_OUTOFMEMORY"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ERROR_OUTOFMEMORY"
diagnosticScenario="Sync failed to recall - ERROR_OUTOFMEMORY"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ERROR_OUTOFMEMORY**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error **ERROR\_OUTOFMEMORY (error code: 0x8007000e or -2147024882)**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to insufficeint memory.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
If the error persists, investigate which application or kernel-mode driver is causing the low memory condition.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



