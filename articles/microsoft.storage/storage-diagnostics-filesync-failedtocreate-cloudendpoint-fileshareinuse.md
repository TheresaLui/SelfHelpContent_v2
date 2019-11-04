<properties
pageTitle="Sync failed to create cloud endpoint - file share in use"
description="Sync failed to create cloud endpoint - file share in use by a different cloud endpoint"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_CloudEndpoint_FileShareInUse"
diagnosticScenario="Sync failed to create cloud endpoint - file share in use by another cloud endpoint"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to create cloud endpoint - file share in use by a different cloud endpoint

<!--issueDescription-->
Cloud endpoint creation failed for sync group(s) under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error: **The specified Azure file share is already in use by a different cloud endpoint**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.
<!--/issueDescription-->

Please refer to [Sync Group Management](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#sync-group-management) for more details on this error.


## **Recommended steps**

If the share is not being used by a cloud endpoint, complete the following steps to clear the Azure File Sync metadata on the Azure file share:
> [!Warning]  
> Deleting the metadata on a share in use by a cloud endpoint will cause Azure File Sync operations to fail.
1. In the Azure portal, go to your Azure file share. 
2. Right-click the Azure file share, and then select Edit metadata.
3. Right-click SyncService, and then select Delete.

## **Recommended Documents**

[Sync Group Management](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#sync-group-management)