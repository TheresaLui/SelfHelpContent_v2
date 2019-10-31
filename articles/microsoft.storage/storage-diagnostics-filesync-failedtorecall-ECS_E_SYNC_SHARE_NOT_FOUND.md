<properties
pageTitle="Sync failed to recall - ECS_E_SYNC_SHARE_NOT_FOUND"
description="Sync failed to recall - ECS_E_SYNC_SHARE_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ECS_E_SYNC_SHARE_NOT_FOUND"
diagnosticScenario="Sync failed to download - ECS_E_CONCURRENCY_CHECK_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed to recall file(s) due to error _**ECS\_E\_SYNC\_SHARE\_NOT\_FOUND**_

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource _**<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**_ due to error **ECS\_E\_SYNC\_SHARE\_NOT\_FOUND** (error code: **0x80c80037** or **-2134376393**). This error occurred between _<!--$startTime-->[startTime]<!--/$startTime-->_ and _<!--$endTime-->[endTime]<!--/$endTime-->_.

This issue occurs if the tiered file was not recalled prior to deleting a server endpoint.
<!--/issueDescription-->

## **Recommended steps**

Tiered files on a server will become inaccessible if the files are not recalled prior to deleting a server endpoint.

Errors logged if tiered files are not accessible
- When syncing a file, error code -2147942467 (0x80070043 - ERROR_BAD_NET_NAME) is logged in the ItemResults event log
- When recalling a file, error code -2134376393 (0x80c80037 - ECS_E_SYNC_SHARE_NOT_FOUND) is logged in the RecallResults event log

Restoring access to your tiered files is possible if the following conditions are met:
- Server endpoint was deleted within past 30 days
- Cloud endpoint was not deleted 
- File share was not deleted
- Sync group was not deleted

If the above conditions are met, you can restore access to the files on the server by recreating the server endpoint at the same path on the server within the same sync group within 30 days. 

If the above conditions are not met, restoring access is not possible as these tiered files on the server are now orphaned. Please follow the instructions below to remove the orphaned tiered files.

**Notes**
- When tiered files are not accessible on the server, the full file should still be accessible if you access the Azure file share directly.
- To prevent orphaned tiered files in the future, follow the steps documented in [Remove a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-endpoint#remove-a-server-endpoint) when deleting a server endpoint.

<a id="get-orphaned"></a>**How to get the list of orphaned tiered files** 

1. Verify Azure File Sync agent version v5.1 or later is installed.
2. Run the following PowerShell commands to list orphaned tiered files:
```powershell
Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"
$orphanFiles = Get-StorageSyncOrphanedTieredFiles -path <server endpoint path>
$orphanFiles.OrphanedTieredFiles > OrphanTieredFiles.txt
```
3. Save the OrphanTieredFiles.txt output file in case files need to be restored from backup after they are deleted.

<a id="remove-orphaned"></a>**How to remove orphaned tiered files** 

*Option 1: Delete the orphaned tiered files*

This option deletes the orphaned tiered files on the Windows Server but requires removing the server endpoint if it exists due to recreation after 30 days or is connected to a different sync group. File conflicts will occur if files are updated on the Windows Server or Azure file share before the server endpoint is recreated.

1. Verify Azure File Sync agent version v5.1 or later is installed.
2. Backup the Azure file share and server endpoint location.
3. Remove the server endpoint in the sync group (if exists) by following the steps documented in [Remove a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-server-endpoint#remove-a-server-endpoint).

> [!Warning]  
> If the server endpoint is not removed prior to using the Remove-StorageSyncOrphanedTieredFiles cmdlet, deleting the orphaned tiered file on the server will delete the full file in the Azure file share. 

4. Run the following PowerShell commands to list orphaned tiered files:

```powershell
Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"
$orphanFiles = Get-StorageSyncOrphanedTieredFiles -path <server endpoint path>
$orphanFiles.OrphanedTieredFiles > OrphanTieredFiles.txt
```
5. Save the OrphanTieredFiles.txt output file in case files need to be restored from backup after they are deleted.
6. Run the following PowerShell commands to delete orphaned tiered files:

```powershell
Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"
$orphanFilesRemoved = Remove-StorageSyncOrphanedTieredFiles -Path <folder path containing orphaned tiered files> -Verbose
$orphanFilesRemoved.OrphanedTieredFiles > DeletedOrphanFiles.txt
```
**Notes** 
- Tiered files modified on the server that are not synced to the Azure file share will be deleted.
- Tiered files which are accessible (not orphan) will not be deleted.
- Non-tiered files will remain on the server.

7. Optional: Recreate the server endpoint if deleted in step 3.

*Option 2: Mount the Azure file share and copy the files locally that are orphaned on the server*

This option doesn’t require removing the server endpoint but requires sufficient disk space to copy the full files locally.

1. [Mount](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-windows) the Azure file share on the Windows Server that has orphaned tiered files.
2. Run the following PowerShell commands to list orphaned tiered files:
```powershell
Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"
$orphanFiles = Get-StorageSyncOrphanedTieredFiles -path <server endpoint path>
$orphanFiles.OrphanedTieredFiles > OrphanTieredFiles.txt
```
3. Use the OrphanTieredFiles.txt output file to identify orphaned tiered files on the server.
4. Overwrite the orphaned tiered files by copying the full file from the Azure file share to the Windows Server.

## **Recommended Documents**

[Tiered files are not accessible on the server after deleting a server endpoint](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#tiered-files-are-not-accessible-on-the-server-after-deleting-a-server-endpoint)

