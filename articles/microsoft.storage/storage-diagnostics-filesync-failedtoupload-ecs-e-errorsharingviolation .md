<properties
pageTitle="Sync failed to upload - ERROR_SHARING_VIOLATION"
description="Sync failed to upload - ERROR_SHARING_VIOLATION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ERROR_SHARING_VIOLATION"
diagnosticScenario="Sync failed to upload - ERROR_SHARING_VIOLATION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to upload file(s) due to error _**ERROR_SHARING_VIOLATION**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070020 or -2147024864**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>The file cannot be synced because it's in use.<br/><br/>
<!--/issueDescription-->


## **Recommended steps**
No action is required. The file will be synced when it's no longer in use.