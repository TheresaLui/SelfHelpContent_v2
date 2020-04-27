 <properties
pageTitle="Sync failed error - ECS_E_MGMT_STORAGEACLSBYPASSNOTSET"
description="Sync failed error - ECS_E_MGMT_STORAGEACLSBYPASSNOTSET"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_MGMT_STORAGEACLSBYPASSNOTSET"
diagnosticScenario="Sync failed error - ECS_E_MGMT_STORAGEACLSBYPASSNOTSET"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_MGMT_STORAGEACLSBYPASSNOTSET
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83096 or -2134364010**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the firewall and virtual network settings are enabled on the storage account and the exception "Allow trusted Microsoft services to access this storage account" is not checked.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, follow the steps documented in the [Configure firewall and virtual network settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings) section in the deployment guide. 

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Configure firewall and virtual network settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)

