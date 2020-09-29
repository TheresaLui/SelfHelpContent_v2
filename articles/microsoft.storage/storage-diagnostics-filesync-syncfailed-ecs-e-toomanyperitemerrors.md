<properties
pageTitle="Sync failed error - ECS_E_TOO_MANY_PER_ITEM_ERRORS"
description="Sync failed error - ECS_E_TOO_MANY_PER_ITEM_ERRORS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_TOO_MANY_PER_ITEM_ERRORS"
diagnosticScenario="Sync failed error - ECS_E_TOO_MANY_PER_ITEM_ERRORS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_TOO_MANY_PER_ITEM_ERRORS
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80253 or -2134375853**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when there are a high number of files that are failing to sync.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To resolve this issue, reduce the number of files that are failing to sync.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


