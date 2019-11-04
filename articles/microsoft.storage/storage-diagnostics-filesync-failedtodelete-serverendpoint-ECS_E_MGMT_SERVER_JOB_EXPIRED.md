<properties
pageTitle="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
description="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToDelete_ServerEndpoint_ECS_E_MGMT_SERVER_JOB_EXPIRED"
diagnosticScenario="Server endpoint deletion failed - ECS_E_MGMT_SERVER_JOB_EXPIRED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync server endpoint deletion failed due to error **ECS\_E\_MGMT\_SERVER\_JOB\_EXPIRED**

<!--issueDescription-->
Server endpoint deletion failed under the Storage Sync Service resource  _**<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->**_ due to error **ECS\_E\_MGMT\_SERVER\_JOB\_EXPIRED** (error code: **-2134347757** or **0x80c87013**). This error occurred between _<!--$startTime-->[startTime]<!--/$startTime-->_ and _<!--$endTime-->[endTime]<!--/$endTime-->_.

This error occurs if the server is offline or doesn't have network connectivity. If the server is no longer available, unregister the server in the portal which will delete the server endpoints. 
<!--/issueDescription-->

## **Recommended steps**
There are several steps that are required to unregister a server with a Storage Sync Service. Let's take a look at how to properly unregister a server.

> [!Warning]  
> Do not attempt to troubleshoot issues with sync, cloud tiering, or any other aspect of Azure File Sync by unregistering and registering a server, or removing and recreating the server endpoints unless explicitly instructed to by a Microsoft engineer. Unregistering a server and removing server endpoints is a destructive operation, and tiered files on the volumes with server endpoints will not be "reconnected" to their locations on the Azure file share after the registered server and server endpoints are recreated, which will result in sync errors. Also note, tiered files that exist outside of a server endpoint namespace may be permanently lost. Tiered files may exist within server endpoints even if cloud tiering was never enabled.

#### (Optional) Recall all tiered data
If you would like files that are currently tiered to be available after removing Azure File Sync (i.e. this is a production, not a test, environment), recall all files on each volume containing server endpoints. Disable cloud tiering for all server endpoints, and then run the following PowerShell cmdlet:

```powershell
Import-Module "C:\Program Files\Azure\StorageSyncAgent\StorageSync.Management.ServerCmdlets.dll"
Invoke-StorageSyncFileRecall -Path <a-volume-with-server-endpoints-on-it>
```

> [!Warning]  
> If the local volume hosting the server endpoint does not have enough free space to recall all the tiered data, the `Invoke-StorageSyncFileRecall` cmdlet will fail.  

#### Remove the server from all sync groups
Before unregistering the server on the Storage Sync Service, all server endpoints on that server must be removed. This can be done via the Azure portal:

1. Navigate to the Storage Sync Service where your server is registered.
2. Remove all server endpoints for this server in each sync group in the Storage Sync Service. This can be accomplished by right-clicking the relevant server endpoint in the sync group pane.

    ![Removing a server endpoint from a sync group](media/storage-sync-files-server-registration/sync-group-server-endpoint-remove-1.png)

This can also be accomplished with a simple PowerShell script:

```powershell
Connect-AzAccount

$storageSyncServiceName = "<your-storage-sync-service>"
$resourceGroup = "<your-resource-group>"

Get-AzStorageSyncGroup -ResourceGroupName $resourceGroup -StorageSyncServiceName $storageSyncServiceName | ForEach-Object { 
    $syncGroup = $_; 
    Get-AzStorageSyncServerEndpoint -ParentObject $syncGroup | Where-Object { $_.ServerEndpointName -eq $env:ComputerName } | ForEach-Object { 
        Remove-AzStorageSyncServerEndpoint -InputObject $_ 
    } 
}
```

#### Unregister the server
Now that all data has been recalled and the server has been removed from all sync groups, the server can be unregistered. 

1. In the Azure portal, navigate to the *Registered servers* section of the Storage Sync Service.
2. Right-click on the server you want to unregister and click "Unregister Server".

    ![Unregister server](media/storage-sync-files-server-registration/unregister-server-1.png)


## **Recommended Documents**
[Unregister a server with Azure File Sync](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-server-registration#unregister-the-server-with-storage-sync-service).