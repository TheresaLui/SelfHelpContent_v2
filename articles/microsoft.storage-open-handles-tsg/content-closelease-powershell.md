<properties
	pageTitle="How to close a file lease using PowerShell"
	description="How to close a file lease using PowerShell"
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
	articleId="88d2fa6e-8c61-4fa2-9fd1-f62ad7ddb624"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# How to close open file handles via PowerShell

A file lease is prevent a file from being modified or deleted. You can check if a file has a file lease with the following PowerShell, replacing \<resource-group>, \<storage-account>, \<file-share>, and \<path-to-file> with the appropriate values for your environment. To remove a lease from a file, you can release the lease or break the lease. To release the lease, you need the LeaseId of the lease, which you set when you create the lease. You do not need the LeaseId to break the lease.

1. Check if a file has a lease

~~~powershell

# Set variables 
$resourceGroupName = "<resource-group>"
$storageAccountName = "<storage-account>"
$fileShareName = "<file-share>"
$fileForLease = "<path-to-file>"

# Get reference to storage account
$storageAccount = Get-AzStorageAccount `
        -ResourceGroupName $resourceGroupName `
        -Name $storageAccountName

# Get reference to file
$file = Get-AzStorageFile `
        -Context $storageAccount.Context `
        -ShareName $fileShareName `
        -Path $fileForLease

$fileClient = $file.ShareFileClient

# Check if the file has a file lease
$fileClient.GetProperties().Value

~~~

2. If a file has a lease, the returned object should contain the following properties:

~~~powershell

LeaseDuration         : Infinite
LeaseState            : Leased
LeaseStatus           : Locked

~~~

3. The following example shows how to break the lease for the file indicated in previous steps.<br />
**Note:** This example continues with the PowerShell variables from above PowerShell block):

~~~powershell

$leaseClient = [Azure.Storage.Files.Shares.Specialized.ShareLeaseClient]::new($fileClient)
$leaseClient.Break() | Out-Null

~~~

