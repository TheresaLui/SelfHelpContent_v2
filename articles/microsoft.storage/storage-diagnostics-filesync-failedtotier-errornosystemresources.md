<properties
pageTitle="Sync failed to tier - ERROR_NO_SYSTEM_RESOURCES"
description="Sync failed to tier - ERROR_NO_SYSTEM_RESOURCES"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ERROR_NO_SYSTEM_RESOURCES"
diagnosticScenario="Sync failed to tier - ERROR_NO_SYSTEM_RESOURCES"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ERROR_NO_SYSTEM_RESOURCES**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x800705aa or -2147023446**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to insufficient system resources.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
If the error persists, investigate which application or kernel-mode driver is exhausting system resources.



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



