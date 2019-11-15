<properties
	pageTitle="Sync failed error - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
	description="Sync failed error - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
    infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
    articleId="FileSync_FailedError_ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
    diagnosticScenario="Sync failed error - ECS_E_AZURE_FILE_SHARE_NOT_FOUND"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed error - ECS_E_AZURE_FILE_SHARE_NOT_FOUND
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c86030 or -2134351824**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the Azure file share is not accessible.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To troubleshoot:
1. [Verify the storage account exists.](#troubleshoot-storage-account)
2. [Ensure the Azure file share exists.](#troubleshoot-azure-file-share)

If the Azure file share was deleted, you need to create a new file share and then recreate the sync group. 
