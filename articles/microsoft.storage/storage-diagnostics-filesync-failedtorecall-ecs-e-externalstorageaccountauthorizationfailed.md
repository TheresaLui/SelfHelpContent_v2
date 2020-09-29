<properties
pageTitle="Sync failed to recall - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
description="Sync failed to recall - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
diagnosticScenario="Sync failed to recall - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ECS_E_AZURE_FILE_SHARE_NOT_FOUND**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c86030 or -2134351824**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the Azure file share is not accessible.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, verify the file share exists and is accessible. If the file share was deleted and recreated, delete and recreate the sync group by performing  the following steps:

1. Delete all server endpoints in the sync group
2. Delete the cloud endpoint
3. Delete the sync group
4. If cloud tiering was enabled on a server endpoint, delete the orphaned tiered files on the server by performing the steps documented in the [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint) section
5. Recreate the sync group

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Sync failed because the Azure file share was deleted and recreated](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134375810)
- [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)


