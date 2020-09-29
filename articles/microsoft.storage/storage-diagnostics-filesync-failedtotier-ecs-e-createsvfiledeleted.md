<properties
pageTitle="Sync failed to tier - ECS_E_CREATE_SV_FILE_DELETED"
description="Sync failed to tier - ECS_E_CREATE_SV_FILE_DELETED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ECS_E_CREATE_SV_FILE_DELETED"
diagnosticScenario="Sync failed to tier - ECS_E_CREATE_SV_FILE_DELETED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ECS_E_CREATE_SV_FILE_DELETED**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83053 or -2134364077**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the file was deleted in the Azure file share.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
No action required. The file should be deleted on the server when the next download sync session runs.


## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



