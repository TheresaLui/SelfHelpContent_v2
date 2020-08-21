<properties
pageTitle="Sync failed error - ECS_E_MGMT_STORAGEACLSNOTSUPPORTED"
description="Sync failed error - ECS_E_MGMT_STORAGEACLSNOTSUPPORTED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_MGMT_STORAGEACLSNOTSUPPORTED"
diagnosticScenario="Sync failed error - ECS_E_MGMT_STORAGEACLSNOTSUPPORTED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_MGMT_STORAGEACLSNOTSUPPORTED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource**<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code 0x80c8306c or -2134364052**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the Azure file share is inaccessible because of a storage account firewall or because the storage account belongs to a virtual network.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, verify the firewall and virtual network settings on the storage account are configured properly. 

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Configure firewall and virtual network settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings).
