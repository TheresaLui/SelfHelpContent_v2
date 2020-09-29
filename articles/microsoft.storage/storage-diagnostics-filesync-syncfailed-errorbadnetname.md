<properties
pageTitle="Sync error - ERROR_BAD_NET_NAME"
description="Sync error - ERROR_BAD_NET_NAME"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_ERROR_BAD_NET_NAME"
diagnosticScenario="Sync error - ERROR_BAD_NET_NAME"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ERROR_BAD_NET_NAME
 
<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070043 or -2147942467**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs if the tiered file was not recalled prior to deleting a server endpoint.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
Restoring access to your tiered files is possible if the following conditions are met:
- Server endpoint was deleted within past 30 days
- Cloud endpoint was not deleted 
- File share was not deleted
- Sync group was not deleted

If the above conditions are met, you can restore access to the files on the server by recreating the server endpoint at the same path on the server within the same sync group within 30 days. 

If the above conditions are not met, restoring access is not possible as these tiered files on the server are now orphaned. Please follow instruction in [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint) to remove the orphaned tiered files.

## **Recommended Documents** 
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)
