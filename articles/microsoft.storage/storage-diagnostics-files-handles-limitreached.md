<properties
pageTitle="File open handles limit exceeded"
description="Too many file handles are open"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_file_openHandlesLimit"
diagnosticScenario="File open handles limit exceeded"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File open handles limit exceeded on <!--$FileType-->[FileType]<!--/$FileType-->

<!--issueDescription-->
The <!--$FileType-->[FileType]<!--/$FileType--> **<!--$FileName-->[FileName]<!--/$FileName-->** has <!--$FileHandleCount-->[FileHandleCount]<!--/$FileHandleCount--> open handles which meet or exceed the open handles limit per file. Please reduce the number of open handles by closing handles for files that is no longer in use.
<!--/issueDescription-->

For more information on the scalability and performance targets of Azure Files, refer to the article [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#azure-files-scale-targets). 

## **Recommended Steps**
The following PowerShell cmdlets can be use to verify and close all open file handles:
1. View open handles for a file share, directory or file using the [Get-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet
2. Close open handles for a file share, directory or file with [Close-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet