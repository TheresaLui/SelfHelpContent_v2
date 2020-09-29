<properties
pageTitle="Sync failed to tier - ERROR_INVALID_FUNCTION"
description="Sync failed to tier - ERROR_INVALID_FUNCTION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToTier_ERROR_INVALID_FUNCTION"
diagnosticScenario="Sync failed to tier - ERROR_INVALID_FUNCTION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to tier file(s) due to error **ERROR_INVALID_FUNCTION**

<!--issueDescription-->
Azure File Sync failed to tier file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070001 or -2147942401**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the cloud tiering filter driver (storagesync.sys) is not running.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, 
1. Open an elevated command prompt and run the following command: `fltmc load storagesync`
2. If the storagesync filter driver fails to load when running the fltmc command, uninstall the Azure File Sync agent, restart the server and reinstall the Azure File Sync agent



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)



