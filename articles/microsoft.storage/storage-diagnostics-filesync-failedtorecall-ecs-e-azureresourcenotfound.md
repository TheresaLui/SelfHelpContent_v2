<properties
pageTitle="Sync failed to recall - ECS_E_AZURE_RESOURCE_NOT_FOUND"
description="Sync failed to recall - ECS_E_AZURE_RESOURCE_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ECS_E_AZURE_RESOURCE_NOT_FOUND"
diagnosticScenario="Sync failed to recall - ECS_E_AZURE_RESOURCE_NOT_FOUND"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ECS_E_AZURE_RESOURCE_NOT_FOUND**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c86002 or -2134351870**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the file is not accessible in the Azure file share.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, verify the file exists in the Azure file share. If the file exists in the Azure file share, upgrade to the latest Azure File Sync latest Azure File Sync [agent version](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#supported-versions).


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Agent version](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#supported-versions)


