<properties
pageTitle="Sync failed error - ECS_E_REPLICA_NOT_READY"
description="Sync failed error - ECS_E_REPLICA_NOT_READY"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_REPLICA_NOT_READY"
diagnosticScenario="Sync failed error - ECS_E_REPLICA_NOT_READY"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_REPLICA_NOT_READY
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8300f or -2134364145**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because change detection is in progress on the Azure file share.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
 No action is required. Sync will resume when change detection completes.

 ## **Recommended Documents**
 
- [Troubleshoot Azure File Sync - Sync Group Management](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#sync-group-management)
