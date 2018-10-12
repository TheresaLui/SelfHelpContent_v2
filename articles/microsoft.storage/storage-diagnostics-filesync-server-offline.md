<properties
pageTitle="One or more servers are not reporting health status"
description="One or more servers are not reporting health status"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt"
displayOrder=""
articleId="FileSync_ServersOffline"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# One of more Azure File Sync registered servers are not reporting health status. 

<!--issueDescription-->
The following Azure File Sync registered servers under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->** are not reporting health status: <br><!--$ServerNameList-->[ServerNameList]<!--/$ServerNameList-->
<!--/issueDescription-->

This issue occurs if the Storage Sync Monitor process is not running or the server is unable to communicate with the Azure File Sync service.

## **Recommended steps**

To resolve this issue, perform the following steps:

1. Open Task Manager on the server and verify the Storage Sync Monitor (AzureStorageSyncMonitor.exe) process is running. If the process is not running, first try restarting the server. If restarting the server does not resolve the issue, upgrade the Azure File Sync agent to version [3.3.0.0]( https://support.microsoft.com/help/4457484/update-rollup-for-azure-file-sync-agent-september-2018) if not currently installed.
2. Verify Firewall and Proxy settings are configured correctly:
	- If the server is behind a firewall, verify port 443 outbound is allowed. If the firewall restricts traffic to specific domains, confirm the domains listed in the Firewall [documentation](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall) are accessible.
	- If the server is behind a proxy, configure the machine-wide or app-specific proxy settings by following the steps in the Proxy [documentation](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy#proxy).
