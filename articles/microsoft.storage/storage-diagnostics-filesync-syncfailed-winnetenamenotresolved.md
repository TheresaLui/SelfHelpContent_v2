<properties
pageTitle="Sync failed error - WININET_E_NAME_NOT_RESOLVED"
description="Sync failed error - WININET_E_NAME_NOT_RESOLVED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_WININET_E_NAME_NOT_RESOLVED"
diagnosticScenario="Sync failed error - WININET_E_NAME_NOT_RESOLVED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - WININET_E_NAME_NOT_RESOLVED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80072ee7 or -2147012889**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error can occur whenever the Azure File Sync service is inaccessible from the server.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To troubleshoot this error, perform the following steps:

1. Verify the Windows service `FileSyncSvc.exe` is not blocked by your firewall
2. Verify that port 443 is open to outgoing connections to the Azure File Sync service with `Test-NetConnection -ComputerName <azure-file-sync-endpoint> -Port 443`. The URL for the `<azure-file-sync-endpoint>` placeholder below can found in the [Azure File Sync proxy and firewall settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall) document.
3. Ensure that the proxy configuration is set as anticipated. This can be done with the `Get-StorageSyncProxyConfiguration` cmdlet. More information on configuring the proxy configuration for Azure File Sync can be found in the [Azure File Sync proxy and firewall settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall).
4. Contact your network administrator for additional assistance troubleshooting network connectivity

Refer to [Azure Latency Test](http://www.azurespeed.com) to test your network latency and speed to the datacenter hosting your storage account.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Azure File Sync proxy and firewall settings](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall)
- [Azure Latency Test](http://www.azurespeed.com)
