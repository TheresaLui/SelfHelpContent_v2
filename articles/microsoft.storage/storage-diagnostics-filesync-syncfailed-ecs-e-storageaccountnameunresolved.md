<properties
pageTitle="Sync failed error - ECS_E_STORAGE_ACCOUNT_NAME_UNRESOLVED"
description="Sync failed error - ECS_E_STORAGE_ACCOUNT_NAME_UNRESOLVED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_STORAGE_ACCOUNT_NAME_UNRESOLVED"
diagnosticScenario="Sync failed error - ECS_E_STORAGE_ACCOUNT_NAME_UNRESOLVED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_STORAGE_ACCOUNT_NAME_UNRESOLVED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83060 or -2134364064)**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the storage account name used could not be resolved.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**

1. Check that you can resolve the storage DNS name from the server with `Test-NetConnection -ComputerName <storage-account-name>.file.core.windows.net -Port 443`
2. [Verify the storage account exists](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-troubleshooting-steps)
3. [Verify the firewall and virtual network settings on the storage account are configured properly (if enabled)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
