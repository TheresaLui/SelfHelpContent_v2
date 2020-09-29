<properties
pageTitle="Sync failed to upload - ECS_E_ACCESS_DENIED_EFS"
description="Sync failed to upload - ECS_E_ACCESS_DENIED_EFS"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ECS_E_ACCESS_DENIED_EFS"
diagnosticScenario="Sync failed to upload - ECS_E_ACCESS_DENIED_EFS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ECS_E_ACCESS_DENIED_EFS**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8027C or -2134375812**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs because the file is encrypted by an unsupported solution (like NTFS EFS).<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, decrypt the file and use a supported encryption solution. For a list of support solutions, see [Encryption solutions](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#encryption-solutions) section in the planning guide.

## **Recommended Documents**

- [Encryption solutions](https://docs.microsoft.com/azure/storage/files/storage-sync-files-planning#encryption-solutions)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


