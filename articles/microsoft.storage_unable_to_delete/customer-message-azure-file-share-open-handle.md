<properties
	pageTitle="Open File Handles"
	description="Open File Handles"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="7e9fb285-c536-42b4-be66-f789f772b191"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Open File Handles

<!--issueDescription-->
We've researched your case and believe that your unable to delete issue is due to open file handles. This resource can not be deleted until all open file handles are closed. We now have PowerShell cmdlets for Azure Files to get the list of open file handles and to close those open file handles. The following steps will help you to resolve this issue. 
<!--/issueDescription-->

## **Recommended Steps**

Install Az PowerShell module version 2.4: 

1. `Install-Module -Name Az`
1. Create a storage account context as follows: `$account = Get-AzStorageAccount -ResourceGroupName myRG -Name mystoraccount $account.Context`
1. Get a list of open file handles using the `Get-AzStorageFileHandle` cmdlet
1. Use `Close-AzStorageFileHandle` to close open handles

* Example 1: List all file handles on a file share recursively: `Get-AzStorageFileHandle -ShareName "mysharename" -Recursive`
* Example 2: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively: `Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive`
* Example 3: Close all file handles on a file: `Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll`

## **Recommended Documents**

* [Install Az PowerShell module version 2.4](https://www.powershellgallery.com/packages/Az/2.4.0)
* [Get-AzStorageFileHandle command reference](https://docs.microsoft.com/powershell/module/az.storage/Get-AzStorageFileHandle?view=azps-2.4.0)
