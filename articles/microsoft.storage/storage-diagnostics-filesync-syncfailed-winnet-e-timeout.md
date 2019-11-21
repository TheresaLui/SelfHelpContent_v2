<properties
pageTitle="Sync failed error - WININET_E_TIMEOUT"
description="Sync failed error - WININET_E_TIMEOUT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_WININET_E_TIMEOUT"
diagnosticScenario="Sync failed error - WININET_E_TIMEOUT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>


# Azure File Sync failed error - WININET_E_TIMEOUT
 
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80072ee2 or -2147012894**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error can occur whenever the Azure File Sync service is inaccessible from the server.<br/><br/>
<!--/issueDescription-->

## **Recommended steps**
To resolve this issue, perform the following steps::

1. Verify the Windows service `FileSyncSvc.exe` is not blocked by your firewall.
2. Verify that port 443 is open to outgoing connections to the Azure File Sync service. You can do this with the `Test-NetConnection` cmdlet. The URL for the `<azure-file-sync-endpoint>` placeholder below can found in the [Azure File Sync proxy and firewall settings](../articles/storage/files/storage-sync-files-firewall-and-proxy.md#firewall) document. 

    ```powershell
    Test-NetConnection -ComputerName <azure-file-sync-endpoint> -Port 443
    ```

3. Ensure that the proxy configuration is set as anticipated. This can be done with the `Get-StorageSyncProxyConfiguration` cmdlet. More information on configuring the proxy configuration for Azure File Sync can be found in the [Azure File Sync proxy and firewall settings](../articles/storage/files/storage-sync-files-firewall-and-proxy.md#firewall).

    ```powershell
    $agentPath = "C:\Program Files\Azure\StorageSyncAgent"
    Import-Module "$agentPath\StorageSync.Management.ServerCmdlets.dll"
    Get-StorageSyncProxyConfiguration
    ```
    
4. Contact your network administrator for additional assistance troubleshooting network connectivity.

on-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80072ee2 or -2147012894**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error can occur whenever the Azure File Sync service is inaccessible from the server.<br/><br/>

## **Recommended steps**
To resolve this issue, perform the following steps::

1. Verify the Windows service `FileSyncSvc.exe` is not blocked by your firewall.
2. Verify that port 443 is open to outgoing connections to the Azure File Sync service. You can do this with the `Test-NetConnection` cmdlet. The URL for the `<azure-file-sync-endpoint>` placeholder below can found in the [Azure File Sync proxy and firewall settings](../articles/storage/files/storage-sync-files-firewall-and-proxy.md#firewall) document. 

    ```powershell
    Test-NetConnection -ComputerName <azure-file-sync-endpoint> -Port 443
    ```

3. Ensure that the proxy configuration is set as anticipated. This can be done with the `Get-StorageSyncProxyConfiguration` cmdlet. More information on configuring the proxy configuration for Azure File Sync can be found in the [Azure File Sync proxy and firewall settings](../articles/storage/files/storage-sync-files-firewall-and-proxy.md#firewall).

    ```powershell
    $agentPath = "C:\Program Files\Azure\StorageSyncAgent"
    Import-Module "$agentPath\StorageSync.Management.ServerCmdlets.dll"
    Get-StorageSyncProxyConfiguration
    ```
    
4. Contact your network administrator for additional assistance troubleshooting network connectivity.

