<properties
	pageTitle="Check if you can renew sync agent certificate"
	description="Check if you can renew sync agent certificate"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32675708"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7b566ef0-de2d-42fa-a9fb-e390fe99b6ca"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to renew sync agent certificate

1. Steps to renew the Sync Agent certificate

~~~powershell

Import-Module 'C:\\Program Files\Azure\StorageSyncAgent\StorageSync.Management.PowerShell.Cmdlets.dll'

Login-AzureRmStorageSync -SubscriptionID $guid$ -TenantID $guid$

Reset-AzureRmStorageSyncServerCertificate -SubscriptionId $guid$ -ResourceGroupName $string$ -StorageSyncServiceName $string$

~~~

2. To get the Tenant ID you can use Az PowerShell module

~~~powershell

Get-AzSubscription -SubscriptionId $Subscription_ID$ | Select TenantId

~~~

3. The Resource Group and StorageSyncServiceName can be found via Az PowerShell

~~~powershell

Get-AzStorageSyncService | Select StorageSyncServicename,ResourceGroupName

~~~
