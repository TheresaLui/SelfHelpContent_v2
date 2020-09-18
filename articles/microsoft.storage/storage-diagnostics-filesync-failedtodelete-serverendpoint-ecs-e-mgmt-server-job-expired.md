<properties
pageTitle="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
description="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDelete_ServerEndpoint_ECS_E_MGMT_SERVER_JOB_EXPIRED"
diagnosticScenario="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync server endpoint deletion failed due to error **ECS_E_MGMT_SERVER_JOB_EXPIRED**

<!--issueDescription-->
Server endpoint deletion failed under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error **"MgmtServerJobExpired" (Error code: -2134347757 or 0x80c87013)**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.

This error occurs if the server is offline or doesn't have network connectivity. If the server is no longer available, unregister the server in the portal which will delete the server endpoints. 
<!--/issueDescription-->

## **Recommended steps**

To delete the server endpoints, perform the following steps:
1. [(Optional) Recall all tiered data](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-registration#optional-recall-all-tiered-data) - If you would like files that are currently tiered to be available after removing Azure File Sync (i.e. this is a production, not a test, environment), recall all files on each volume containing server endpoints
2. [Remove the server from all sync groups](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-registration#remove-the-server-from-all-sync-groups) - Before unregistering the server on the Storage Sync Service, all server endpoints on that server must be removed. This can be done via the Azure portal
3. [Unregister the server](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-registration#unregister-the-server) - Now that all data has been recalled and the server has been removed from all sync groups, the server can be unregistered

## **Recommended Documents**
- [Unregister a server with Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-registration#unregister-the-server-with-storage-sync-service)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347757)