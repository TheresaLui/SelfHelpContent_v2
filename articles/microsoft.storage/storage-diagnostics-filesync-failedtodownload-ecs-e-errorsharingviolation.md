<properties
pageTitle="Sync failed to download - ERROR_SHARING_VIOLATION"
description="Sync failed to download - ERROR_SHARING_VIOLATION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDownload_ERROR_SHARING_VIOLATION"
diagnosticScenario="Sync failed to download - ERROR_SHARING_VIOLATION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to download file(s) due to error _**ERROR_SHARING_VIOLATION**_

<!--issueDescription-->
Azure File Sync failed to download file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**  due to **error code: 0x80070020 or -2147024864**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the file cannot be synced because it's in use.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**

No action is required. The file will be synced when it's no longer in use.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

