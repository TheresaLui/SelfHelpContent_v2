<properties
	pageTitle="How to check proxy settings"
	description="How to check proxy settings"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9d1f8f86-7dbc-4128-9455-15a2038ed9c8"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check proxy settings

If the server is behind a proxy, you need to configure the machine-wide or app-specific proxy settings

**App-settings**

App-specific proxy settings allow configuration of a proxy specifically for Azure File Sync traffic. App-specific proxy settings are supported on agent version 4.0.1.0 or newer and can be configured during the agent installation or by using

PowerShell commands to configure app-specific proxy settings:

~~~powershell

Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"

Set-StorageSyncProxyConfiguration -Address  -Port  -ProxyCredential

~~~

**Machine-wide proxy settings**

Machine-wide proxy settings are transparent to the Azure File Sync agent as the entire traffic of the server is routed through the proxy. To configure machine-wide proxy settings, follow the steps below:

[Proxy Issues](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy#proxy)
