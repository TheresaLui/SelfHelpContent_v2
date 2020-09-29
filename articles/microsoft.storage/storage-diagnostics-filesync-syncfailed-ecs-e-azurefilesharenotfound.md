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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_AZURE_FILE_SHARE_NOT_FOUND
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c86030 or -2134351824**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the Azure file share is not accessible.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To troubleshoot:

Verify the storage account exists by performing the following steps:
1. Navigate to the sync group within the Storage Sync Service
2. Select the cloud endpoint within the sync group
3. Note the Azure file share name in the opened pane
4. Select the linked storage account. If this link fails, the referenced storage account has been removed
   
Ensure the Azure file share exists by performing the following steps:
1. Click **Overview** on the left-hand table of contents to return to the main storage account page
2. Select **Files** to view the list of file shares
3. Verify the file share referenced by the cloud endpoint appears in the list of file shares (you should have noted this in step 1 above)

If the Azure file share was deleted, you need to create a new file share and then recreate the sync group

## **Recommended Documents**
- [Common Troubleshooting Steps](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#common-troubleshooting-steps)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
