<properties
pageTitle="Sync failed error - ERROR_ACCESS_DENIED"
description="Sync failed error - ERROR_ACCESS_DENIED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ERROR_ACCESS_DENIED"
diagnosticScenario="Sync failed error - ERROR_ACCESS_DENIED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ACCESS_DENIED

<!--issueDescription-->

Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80070005 or -2147024891** . This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error can occur if the NT AUTHORITY\SYSTEM account does not have permissions to the System Volume Information folder on the volume where the server endpoint is located.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the following steps:

1. Download [Psexec](https://docs.microsoft.com/sysinternals/downloads/psexec) tool.
2. Run the following command from an elevated command prompt to launch a command prompt using the system account: **PsExec.exe -i -s -d cmd** 
3. From the command prompt running under the system account, run the following command to confirm the NT AUTHORITY\SYSTEM account does not have access to the System Volume Information folder: **cacls "drive letter:\system volume information" /T /C**
4. If the NT AUTHORITY\SYSTEM account does not have access to the System Volume Information folder, run the following command: **cacls  "drive letter:\system volume information" /T /E /G "NT AUTHORITY\SYSTEM:F"**
	- If step #4 fails with access denied, run the following command to take ownership of the System Volume Information folder and then repeat step #4: **takeown /A /R /F "drive letter:\System Volume Information"**

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [PsExec](https://docs.microsoft.com/sysinternals/downloads/psexec)
