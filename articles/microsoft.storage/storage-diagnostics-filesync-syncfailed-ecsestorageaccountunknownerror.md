<properties
pageTitle="Sync failed error - ECS_E_STORAGE_ACCOUNT_UNKNOWN_ERROR"
description="Sync failed error - ECS_E_STORAGE_ACCOUNT_UNKNOWN_ERROR"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_STORAGE_ACCOUNT_UNKNOWN_ERROR"
diagnosticScenario="Sync failed error - ECS_E_STORAGE_ACCOUNT_UNKNOWN_ERROR"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>



# Azure File Sync failed error - ECS_E_STORAGE_ACCOUNT_UNKNOWN_ERROR 

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8308a or -2134364022**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This errors occurs when the storage account is unknown.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue,

1. Verify the storage account exists by performing the following steps in azure portal:
    - Navigate to the sync group within the Storage Sync Service
    - Select the cloud endpoint within the sync group
    - Note the Azure file share name in the opened pane
    - Select the linked storage account. If this link fails, the referenced storage account has been removed
   
 2. [Verify the firewall and virtual network settings on the storage account are configured properly (if enabled)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Verify the firewall and virtual network settings on the storage account are configured properly (if enabled)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)
