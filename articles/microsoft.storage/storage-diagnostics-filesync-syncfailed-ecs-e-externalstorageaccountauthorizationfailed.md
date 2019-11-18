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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed error - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8305f or -2134364065**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the Azure File Sync agent cannot access the Azure file share, which may be because the Azure file share or the storage account hosting it no longer exists.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
 You can troubleshoot this error by working through the following steps:

1. [Verify the storage account exists.](#troubleshoot-storage-account)
2. [Ensure the Azure file share exists.](#troubleshoot-azure-file-share)
3. [Ensure Azure File Sync has access to the storage account.](#troubleshoot-rbac)
4. [Verify the firewall and virtual network settings on the storage account are configured properly (if enabled)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)

