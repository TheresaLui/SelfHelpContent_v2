<properties
pageTitle="Sync failed to upload - ECS_E_AZURE_AUTHORIZATION_FAILED"
description="Sync failed to upload - ECS_E_AZURE_AUTHORIZATION_FAILED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_AZURE_AUTHORIZATION_FAILED"
diagnosticScenario="Sync failed to upload - ECS_E_AZURE_AUTHORIZATION_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_AZURE_AUTHORIZATION_FAILED**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c86044 or -2134351804**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file cannot be synced because the firewall and virtual network settings on the storage account are enabled and the server does not have access to the storage account.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, add the Server IP address or virtual network by performing the following steps:

1. From the Azure portal, navigate to the storage account you want to secure
1. Select the **Firewalls and virtual networks** button on the left menu
1. Select **Selected networks** under **Allow access from**
1. Make sure your servers IP or virtual network is listed under the appropriate section
1. Make sure **Allow trusted Microsoft services to access this storage account** is checked
1. Select **Save** to save your settings

## **Recommended Documents**
- [Configure firewall and virtual network settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
