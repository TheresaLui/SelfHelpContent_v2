<properties
pageTitle="FileSync broken tiered files"
description="There are broken tiered files on the server endpoint"
infoBubbleText="See details on right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncPerItemError_BrokenGhosts"
diagnosticScenario="FileSync broken ghosts"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File Sync failed to upload **<!--$TotalFileCount-->[TotalFileCount]<!--/$TotalFileCount-->** broken tiered file(s)

<!--issueDescription-->
File Sync failed to upload **<!--$TotalFileCount-->[TotalFileCount]<!--/$TotalFileCount-->** broken tiered file(s) for server endpoints under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->**. These tiered files have been rendered non-functional as the server endpoint was deleted without first recalling all the tiered data to the server. These files cannot be synced, and must be cleaned up. Below is the distribution of broken tiered files per server endpoint:<br> <!--$ServerEndpointList-->[ServerEndpointList]<!--/$ServerEndpointList-->
<!--/issueDescription-->

Please follow the troubleshooting steps [documented here](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot#i-deleted-and-recreated-my-server-endpoint-and-now-files-arent-syncing).
<br> 

