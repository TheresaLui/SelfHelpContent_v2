<properties
pageTitle="Server endpoint creation failed - ECS_E_COMPRESSION_UNSUPPORTED"
description="Server endpoint creation failed - ECS_E_COMPRESSION_UNSUPPORTED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToCreate_ServerEndpoint_ECS_E_COMPRESSION_UNSUPPORTED"
diagnosticScenario="Server endpoint creation failed - ECS_E_COMPRESSION_UNSUPPORTED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to create server endpoint creation failed due to error ECS\_E\_COMPRESSION\_UNSUPPORTED

<!--issueDescription-->
Server endpoint creation failed under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error **ECS\_E\_COMPRESSION\_UNSUPPORTED** (error code: -2134347507 or 0x80c8710d). This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.
<!--/issueDescription-->

This error occurs because Azure File Sync does not support server endpoints on volumes which have a compressed System Volume Information folder.


## **Recommended steps**

Decompress the System Volume Information folder. If the System Volume Information folder is the only folder compressed on the volume, perform the following steps:
1. Download [PsExec](https://docs.microsoft.com/sysinternals/downloads/psexec) tool.
2. Run the following command from an elevated command prompt to launch a command prompt running under the system account: PsExec.exe -i -s -d cmd
3. From the command prompt running under the system account, type the following commands and hit enter:
    >cd /d "drive letter:\System Volume

## **Recommended Documents**

- [Sync group management](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#sync-group-management)
- [PsExec](https://docs.microsoft.com/sysinternals/downloads/psexec)
