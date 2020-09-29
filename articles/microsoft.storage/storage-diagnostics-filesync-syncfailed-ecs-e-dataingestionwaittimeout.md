<properties
pageTitle="Sync failed error - ECS_E_DATA_INGESTION_WAIT_TIMEOUT"
description="Sync failed error - ECS_E_DATA_INGESTION_WAIT_TIMEOUT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_DATA_INGESTION_WAIT_TIMEOUT"
diagnosticScenario="Sync failed error - ECS_E_DATA_INGESTION_WAIT_TIMEOUT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>


# Azure File Sync failed error - ECS_E_DATA_INGESTION_WAIT_TIMEOUT

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83085 or -2134364027**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when a data ingestion operation exceeds the timeout.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action is required.This error can be ignored if sync is making progress (AppliedItemCount is greater than 0). 

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


