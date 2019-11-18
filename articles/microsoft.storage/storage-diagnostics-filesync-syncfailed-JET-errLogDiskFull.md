<properties
	pageTitle="Sync failed error - JET_errLogDiskFull "
	description="Sync failed error - JET_errLogDiskFull"
    infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
    articleId="FileSync_FailedError_JET_errLogDiskFull"
    diagnosticScenario="Sync failed error - JET_errLogDiskFull "
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed error - JET_Error_Log_Disk_Full 
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x8e5e0211 or -1906441711**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the volume has filled up. This error commonly occurs because files outside the server endpoint are using up space on the volume.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To resolve this issue, free up space on the volume by adding additional server endpoints, moving files to a different volume, or increasing the size of the volume the server endpoint is on.
