<properties
pageTitle="Server endpoint creation failed - server endpoints limit reached "
description="Server endpoint creation failed -server endpoints limit reached"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_SERVERENDPOINTS_LIMIT_REACHED"
diagnosticScenario="Sync failed to create server endpoint - ServerendpointsLimitReached"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint - Server endpoints limit reached

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: -2134376345 or 0x80c80067**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the server endpoints per server limit is reached. Azure File Sync currently supports up to 30 server endpoints per server. 
<!--/issueDescription-->

## **Recommended Documents**

- [Azure File Sync scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#azure-file-sync-scale-targets)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
