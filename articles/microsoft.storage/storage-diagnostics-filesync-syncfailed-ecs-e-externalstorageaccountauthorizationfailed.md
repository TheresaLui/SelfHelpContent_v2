<properties
pageTitle="Sync failed error - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
description="Sync failed error - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
diagnosticScenario="Sync failed error - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8305f or -2134364065**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the Azure File Sync agent cannot access the Azure file share, which may be because the Azure file share or the storage account hosting it no longer exists.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
 You can troubleshoot this error by working through the following steps:

1. [Verify the storage account exists](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-troubleshooting-steps)
2. [Ensure the Azure file share exists](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-troubleshooting-steps)
3. [Ensure Azure File Sync has access to the storage account](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-troubleshooting-steps)
4. [Verify the firewall and virtual network settings on the storage account are configured properly (if enabled)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
