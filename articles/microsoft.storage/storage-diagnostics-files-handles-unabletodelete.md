<properties
pageTitle="Unable to delete file due to open handles"
description="File handles must be closed before deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_unableToDelete_file_openHandles"
diagnosticScenario="Open file handles prevents file deletion"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to delete <!--$FileType-->[FileType]<!--/$FileType--> due to open handles

<!--issueDescription-->
The Azure File Storage **<!--$FileName-->[FileName]<!--/$FileName-->** cannot be deleted because it contains <!--$FileHandleCount-->[FileHandleCount]<!--/$FileHandleCount--> open handles. All handles need to be closed before the file can be deleted.
<!--/issueDescription-->

For more information, refer to the article [Azure file share – failed to delete files from Azure file share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-cannot-delete-files-azure-file-share).

## **Recommended Steps**
The following PowerShell cmdlets can be use to verify and close all open file handles before the <!--$FileType-->[FileType]<!--/$FileType--> can be deleted:
1. View open handles for a file share, directory or file using the [Get-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet
2. Close open handles for a file share, directory or file with [Close-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet