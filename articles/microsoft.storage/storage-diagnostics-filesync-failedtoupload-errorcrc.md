<properties
pageTitle="Sync failed to upload - ERROR_CRC"
description="Sync failed to upload - ERROR_CRC"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToUpload_ERROR_CRC"
diagnosticScenario="Sync failed to upload - ERROR_CRC"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to upload file(s) due to error _**ERROR_CRC**_

<!--issueDescription-->
Azure File Sync failed to upload file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070017 or -2147024873**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This issue occurs if a tiered file was not recalled prior to deleting a server endpoint or if the file is corrupt.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, 

1. Remove tiered files that are orphaned by performing the steps in [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)

2. If the error continues to occur after removing orphaned tiered files, run [chkdsk](https://docs.microsoft.com/windows-server/administration/windows-commands/chkdsk) on the volume



## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)
- [Chkdsk](https://docs.microsoft.com/windows-server/administration/windows-commands/chkdsk)
