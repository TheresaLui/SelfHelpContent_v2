<properties
pageTitle="Sync failed error - ECS_E_STORAGE_ACCOUNT_FAILED_OVER"
description="Sync failed error - ECS_E_STORAGE_ACCOUNT_FAILED_OVER"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storageaccounts"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_STORAGE_ACCOUNT_FAILED_OVER"
diagnosticScenario="Sync failed error - ECS_E_STORAGE_ACCOUNT_FAILED_OVER"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Azure File Sync failed error - ECS_E_STORAGE_ACCOUNT_FAILED_OVER
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83073 or -2134364045**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the storage account has failed over to another region. Azure File Sync does not support the storage account failover feature. Storage accounts containing Azure file shares being used as cloud endpoints in Azure File Sync should not be failed over. Doing so will cause sync to stop working and may also cause unexpected data loss in the case of newly tiered files.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, move the storage account to the primary region.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
