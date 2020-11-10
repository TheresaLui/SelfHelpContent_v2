<properties
pageTitle="Sync failed error - ECS_E_STORAGE_ACCOUNT_LOCKED"
description="Sync failed error - ECS_E_STORAGE_ACCOUNT_LOCKED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_STORAGE_ACCOUNT_LOCKED"
diagnosticScenario="Sync failed error - ECS_E_STORAGE_ACCOUNT_LOCKED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>


# Azure File Sync failed error - ECS_E_STORAGE_ACCOUNT_LOCKED 
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83092 or -2134364014**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the storage account has a read-only resource lock.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, remove the read-only resource lock on the storage account.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Resource lock](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources)

