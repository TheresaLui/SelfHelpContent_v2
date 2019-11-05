<properties
pageTitle="Sync failed to recall - ECS_E_SYNC_SHARE_NOT_FOUND"
description="Sync failed to recall - ECS_E_SYNC_SHARE_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ECS_E_SYNC_SHARE_NOT_FOUND"
diagnosticScenario="Sync failed to download - ECS_E_CONCURRENCY_CHECK_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to recall file(s) due to error _**ECS\_E\_SYNC\_SHARE\_NOT\_FOUND**_

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error **ECS_E_SYNC_SHARE_NOT_FOUND** (error code: 0x80c80037 or -2134376393). This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.

This issue occurs if the tiered file was not recalled prior to deleting a server endpoint.
<!--/issueDescription-->

## **Recommended steps**

Restoring access to your tiered files is possible if the following conditions are met:
- Server endpoint was deleted within past 30 days
- Cloud endpoint was not deleted 
- File share was not deleted
- Sync group was not deleted

If the above conditions are met, you can restore access to the files on the server by recreating the server endpoint at the same path on the server within the same sync group within 30 days. 

If the above conditions are not met, restoring access is not possible as these tiered files on the server are now orphaned. Please follow the instructions below to remove the orphaned tiered files.

**Notes**
- When tiered files are not accessible on the server, the full file should still be accessible if you access the Azure file share directly.
- To prevent orphaned tiered files in the future, follow the steps documented in [Remove a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-endpoint#remove-a-server-endpoint) when deleting a server endpoint.

**How to remove orphaned tiered files** 

*Option 1: Delete the orphaned tiered files*
This option deletes the orphaned tiered files on the Windows Server but requires removing the server endpoint if it exists due to recreation after 30 days or is connected to a different sync group. File conflicts will occur if files are updated on the Windows Server or Azure file share before the server endpoint is recreated.

*Option 2: Mount the Azure file share and copy the files locally that are orphaned on the server*

This option doesn’t require removing the server endpoint but requires sufficient disk space to copy the full files locally.

## **Recommended Documents**

[Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)

