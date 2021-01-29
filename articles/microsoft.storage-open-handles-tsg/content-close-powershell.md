<properties
	pageTitle="How to close open file handles via PowerShell"
	description="How to close open file handles via PowerShell"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="d376cb98-b6a5-4c36-b68d-ea79f6104308"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to close open file handles via PowerShell

Make sure that you meet the requirements to perform this task by checking the points below:

1. Install latest version of Az PowerShell module. [www.powershellgallery.com/packages/Az/](https://www.powershellgallery.com/packages/Az/)
2. Install-Module -Name Az
3. Create a Storage Account context:
     * $account = Get-AzStorageAccount -ResourceGroupName myRG -Name mystoraccount
     * $account.Context

**Get the list of open file handles**

1. **Use [Get-AzStorageFileHandle](https://docs.microsoft.com/en-gb/powershell/module/az.storage/get-azstoragefilehandle?view=azps-3.3.0)**
2. Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime

~~~powershell

Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929

~~~

3. Example 2: List first 2 file handles on a file directory recursively

~~~powershell

Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049

~~~

**Close open file handles**

1. **Use [Close-AzStorageFileHandle](https://docs.microsoft.com/en-gb/powershell/module/az.storage/close-azstoragefilehandle?view=azps-3.3.0)**
2. Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.

~~~powershell

Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive

~~~

3. Example 2: Close all file handles on a file directory recursively and show the closed file handle count

~~~powershell

Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10

~~~
