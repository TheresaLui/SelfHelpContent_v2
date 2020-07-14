<properties
pageTitle="One or more servers are not reporting health status"
description="One or more servers are not reporting health status"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt24"
ms.author="jeffpatt"
displayOrder=""
articleId="FileSync_ServersOffline"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# One of more Azure File Sync servers are not reporting health status

<!--issueDescription-->
The following Azure File Sync registered server(s) under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->** are not reporting health status:

<!--$ServerNameList-->[ServerNameList]<!--/$ServerNameList-->
<!--/issueDescription-->

This issue occurs if the Storage Sync Monitor process is not running or the server is unable to communicate with the Azure File Sync service.

## **Recommended Steps**

To resolve this issue, perform the following steps:

1. Verify the server is online and has network connectivity. If the server is behind a firewall or proxy, perform the following steps:

	- If the server is behind a firewall, verify port 443 outbound is allowed. If the firewall restricts traffic to specific domains, confirm the domains listed in the firewall [documentation](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall) are accessible.
	- If the server is behind a proxy, configure the machine-wide or app-specific proxy settings by following the steps in the proxy [documentation](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#proxy)

2. Open Task Manager on the server and verify the Storage Sync Monitor (AzureStorageSyncMonitor.exe) process is running. If the process is not running, first try restarting the server. If restarting the server does not resolve the issue, upgrade to the latest Azure File Sync [agent version](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes).
