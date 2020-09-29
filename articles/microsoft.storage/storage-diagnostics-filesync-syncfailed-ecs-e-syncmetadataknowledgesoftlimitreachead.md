<properties
pageTitle="Sync failed error - ECS_E_SYNC_METADATA_KNOWLEDGE_SOFT_LIMIT_REACHED"
description="Sync failed error - ECS_E_SYNC_METADATA_KNOWLEDGE_SOFT_LIMIT_REACHED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_SYNC_METADATA_KNOWLEDGE_SOFT_LIMIT_REACHED"
diagnosticScenario="Sync failed error - ECS_E_SYNC_METADATA_KNOWLEDGE_SOFT_LIMIT_REACHED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_SYNC_METADATA_KNOWLEDGE_SOFT_LIMIT_REACHED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code 0x80c8023b or -2134375877**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when there are a high number of files that are failing to sync.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To resolve this issue, reduce the number of files that are failing to sync.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


