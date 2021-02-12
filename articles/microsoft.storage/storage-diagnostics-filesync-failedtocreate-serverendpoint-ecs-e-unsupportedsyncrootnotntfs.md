<properties
pageTitle="Server endpoint creation failed - ECS_E_UNSUPPORTED_SYNCROOT_NOT_NTFS"
description="Server endpoint creation failed - ECS_E_UNSUPPORTED_SYNCROOT_NOT_NTFS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_UNSUPPORTED_SYNCROOT_NOT_NTFS"
diagnosticScenario="Server endpoint creation failed - ECS_E_UNSUPPORTED_SYNCROOT_NOT_NTFS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to create server endpoint creation failed due to error ECS_E_UNSUPPORTED_SYNCROOT_NOT_NTFS

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code -2134375640 or 0x80c80328**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the server endpoint path specified is not an NTFS volume.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, verify the server endpoint path specified is a locally attached NTFS volume. Note, Azure File Sync does not support mapped drives as a server endpoint path.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

