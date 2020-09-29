<properties
pageTitle="Sync failed error - session canceled "
description="Sync failed error - session canceled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ERROR_CANCELLED"
diagnosticScenario="Sync failed error - session canceled"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - canceled

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**due to **error code: 0x800704c7 or -2147023673**. This error occurred between  **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the sync session is cancelled due to a server restart or a VSS snapshot was created to sync files with open handles.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action is required. If this error persists for longer than a day, please file an ICM ticket.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
