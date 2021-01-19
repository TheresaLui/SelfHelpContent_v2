<properties
	pageTitle="Check if you can reset sync server"
	description="Check if you can reset sync server"
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
	articleId="87e6ec56-4041-4ce8-b2b8-fd415caa5e4e"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to reset the sync server

1. Make sure there are no other sync services which are using this server.
2. If you see in portal if this server is being used by other sync services, unregister and delete it.
3. The registered server object represents a trust relationship between your server (or cluster) and the Storage Sync Service. 
4. You can register as many servers to a Storage Sync Service instance as you want.
5. However, a server (or cluster) can be registered with only one Storage Sync Service at a time.
6. Open Powershell in admin mode and run these commands

~~~powershell

Remove-ItemProperty HKLM:\SOFTWARE\Microsoft\Azure\StorageSync\ServerSetting -Name ServerSetting.Server=Localhost -Force

Reset-AzureRmStorageSyncServer #this will reset the server ID which means that you will have to re-do the server registration from scratch.

~~~

7. Now retry server registration.  
8. In my case it wouldn't recognize the powershell cmdlet.  
9. You need to manually import the Storage Sync module

~~~powershell

Import-Module AzureRM.StorageSync -verbose

Login-AzureRmStorageSync

Import-Module AzureRM.StorageSync -verbose

Register-AzureRmStorageSyncServer -StorageSyncServiceName afswikisyncsvc -MonitoringDataPath E:\FileSync2 -ResourceGroupName AFS -SubscriptionId 6c207442-3f5d-47e6-a359-07986e649df8

~~~

10. To know more about Sync commands, run the below query in powershell

~~~powershell

ipmo 'C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll' -Verbose

~~~

11. This will give all the cmdlets in this module
