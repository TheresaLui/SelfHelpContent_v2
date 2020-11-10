<properties
pageTitle="Sync failed error - ECS_E_INVALID_AAD_TENANT"
description="Sync failed error - ECS_E_INVALID_AAD_TENANT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_INVALID_AAD_TENANT"
diagnosticScenario="Sync failed error - ECS_E_INVALID_AAD_TENANT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_INVALID_AAD_TENANT
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83088 or -2134364024**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because Azure File Sync does not currently support moving the subscription to a different Azure Active Directory tenant.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform one of the following options:

- **Option 1 (recommended)**: Move the subscription back to the original Azure Active Directory tenant
- **Option 2**: Delete and recreate the current sync group. If cloud tiering was enabled on the server endpoint, delete the sync group and then perform the steps documented in the [Cloud Tiering section]( https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint) to remove the orphaned tiered files prior to recreating the sync groups. 

## **Recommended Documents**

- [Cloud Tiering section]( https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
