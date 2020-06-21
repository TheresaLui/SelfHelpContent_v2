<properties
pageTitle="Sync failed to recall - ERROR_SEM_TIMEOUT"
description="Sync failed to recall - ERROR_SEM_TIMEOUT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ERROR_SEM_TIMEOUT"
diagnosticScenario="Sync failed to recall - ERROR_SEM_TIMEOUT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ERROR_SEM_TIMEOUT**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070079 or -2147024775**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue is typically caused by high network latency. 
<!--/issueDescription-->

## **Recommended Steps**
No action required. If the error persists for several hours, please open a support case.

Refer to [Azure Latency Test](http://www.azurespeed.com) to test your network latency and speed to the datacenter hosting your storage account.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Azure Latency Test](http://www.azurespeed.com)
