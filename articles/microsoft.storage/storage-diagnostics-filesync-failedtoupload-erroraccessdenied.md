<properties
pageTitle="Sync failed to upload - ERROR_ACCESS_DENIED"
description="Sync failed to upload - ERROR_ACCESS_DENIED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ERROR_ACCESS_DENIED"
diagnosticScenario="Sync failed to upload - ERROR_ACCESS_DENIED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to upload file(s) due to error _**ACCESS_DENIED**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070005 or -2147024891**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file has a delete pending state.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
No action is required. The file will be deleted once all open file handles are closed.

## **Recommended Documents**

[Troubleshoot Azure File Sync - Sync Group Management](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#sync-group-management)
