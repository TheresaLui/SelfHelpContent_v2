<properties
pageTitle="Sync failed to upload - ECS_E_SECURITY_DESCRIPTOR_SIZE_TOO_LARGE"
description="Sync failed to upload - ECS_E_SECURITY_DESCRIPTOR_SIZE_TOO_LARGE"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_SECURITY_DESCRIPTOR_SIZE_TOO_LARGE"
diagnosticScenario="Sync failed to upload - ECS_E_SECURITY_DESCRIPTOR_SIZE_TOO_LARGE"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_SECURITY_DESCRIPTOR_SIZE_TOO_LARGE**_

<!--issueDescription-->

Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80243 or -2134375869**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs when the file cannot be synced because the security descriptor size exceeds the 64 KiB limit.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, remove access control entries (ACE) on the file to reduce the security descriptor size.

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
