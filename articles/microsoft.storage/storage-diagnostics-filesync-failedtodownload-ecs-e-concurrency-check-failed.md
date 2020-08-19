<properties
pageTitle="Sync failed to download - ECS_E_CONCURRENCY_CHECK_FAILED"
description="Sync failed to download - ECS_E_CONCURRENCY_CHECK_FAILED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDownload_ECS_E_CONCURRENCY_CHECK_FAILED"
diagnosticScenario="Sync failed to download - ECS_E_CONCURRENCY_CHECK_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to download file(s) due to error _**ECS_E_CONCURRENCY_CHECK_FAILED**_

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error code: 0x80c8031d or -2134375651**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.

This issue occurs because the file has changed, but the file change has not yet been detected by sync.
<!--/issueDescription-->

## **Recommended steps**

No action is required. The file will sync once the change is detected.

## **Recommended Documents**

[How do I see if there are specific files or folders that are not syncing?](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#how-do-i-see-if-there-are-specific-files-or-folders-that-are-not-syncing)