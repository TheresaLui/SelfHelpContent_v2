<properties
pageTitle="Sync failed to recall - ERROR_ACCESS_DENIED"
description="Sync failed to recall - ERROR_ACCESS_DENIED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ERROR_ACCESS_DENIED"
diagnosticScenario="Sync failed to recall - ERROR_ACCESS_DENIED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ERROR_ACCESS_DENIED**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070005 or -2147024891**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to an access denied error. This issue can occur if the firewall and virtual network settings on the storage account are enabled and the server does not have access to the storage account. 
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, add the Server IP address or virtual network by performing the following the steps in the Azure portal:

1. From the Azure portal, navigate to the storage account you want to secure
1. Select the **Firewalls and virtual networks** button on the left menu
1. Select **Selected networks** under **Allow access from**
1. Make sure your servers IP or virtual network is listed under the appropriate section
1. Make sure **Allow trusted Microsoft services to access this storage account** is checked
1. Select **Save** to save your settings

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Configure firewall and virtual network settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-deployment-guide?tabs=azure-portal#configure-firewall-and-virtual-network-settings)
