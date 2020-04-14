<properties
pageTitle="Sync failed to tier - WININET_E_NAME_NOT_RESOLVED"
description="Sync failed to tier - WININET_E_NAME_NOT_RESOLVED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_WININET_E_NAME_NOT_RESOLVED"
diagnosticScenario="Sync failed to tier - WININET_E_NAME_NOT_RESOLVED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **WININET_E_NAME_NOT_RESOLVED**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80072ee7 or -2147012889**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to a network issue.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action required. If the error persists, check network connectivity to the Azure file share.

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)