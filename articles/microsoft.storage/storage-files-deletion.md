<properties
	pageTitle="Unable to delete file in an Azure file share"
	description=" Unable to delete file in an Azure file share"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="jeffpatt24"
	ms.author="jeffpatt"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=" 32736816"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	articleId="Unable to delete file in an Azure file share"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshooting Azure Files deletion issues

## **Recommended Documents**    

The following PowerShell cmdlets can be use to verify and close all open file handles 

1. View open handles for a file share, directory or file using the [Get-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet
2. Close open handles for a file share, directory or file with [Close-AzStorageFileHandle](https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle?view=azps-3.5.0) PowerShell cmdlet
3. [Unable to delete a file or directory in Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#open-handles)
