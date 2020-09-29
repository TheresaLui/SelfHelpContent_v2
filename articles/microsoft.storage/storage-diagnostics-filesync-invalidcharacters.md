<properties
pageTitle="Sync error - invalid characters"
description="Sync is failing for some files because they contain unsupported characters"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncPerItemError_InvalidCharacters"
diagnosticScenario="Sync error - invalid characters"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File Sync failed to upload **<!--$TotalFileCount-->[TotalFileCount]<!--/$TotalFileCount-->** file(s) due to unsupported characters in the file name(s)

<!--issueDescription-->
File Sync failed to upload **<!--$TotalFileCount-->[TotalFileCount]<!--/$TotalFileCount-->** file(s) as they contain one or more unsupported characters for server endpoints under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->**. Below is the distribution of files with unsupported characters per server endpoint:
<!--$ServerEndpointList-->[ServerEndpointList]<!--/$ServerEndpointList-->
<!--/issueDescription-->

## **Recommended steps**

For these files to sync, you must remove or rename the files with unsupported characters. 
See [this document](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cportal#how-do-i-see-if-there-are-specific-files-or-folders-that-are-not-syncing) for details on unsupported characters and how to identify the files.

## **Recommended Documents**

[How do I see if there are specific files or folders that are not syncing?](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cportal#how-do-i-see-if-there-are-specific-files-or-folders-that-are-not-syncing)

