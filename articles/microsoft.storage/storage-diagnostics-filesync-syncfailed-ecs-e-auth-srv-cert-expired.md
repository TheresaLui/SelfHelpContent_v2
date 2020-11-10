<properties
pageTitle="Sync failed error - ECS_E_AUTH_SRV_CERT_EXPIRED "
description="Sync failed error - ECS_E_AUTH_SRV_CERT_EXPIRED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_AUTH_SRV_CERT_EXPIRED"
diagnosticScenario="Sync failed error - ECS_E_AUTH_SRV_CERT_EXPIRED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_AUTH_SRV_CERT_EXPIRED
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c83078 or -2134364040**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the certificate used for authentication is expired.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To confirm the certificate is expired, perform the following steps:  

1. Open the Certificates MMC snap-in, select Computer Account and navigate to Certificates (Local Computer)\Personal\Certificates
2. Check if the client authentication certificate is expired

If the client authentication certificate is expired, perform the following steps to resolve the issue:

1. Verify Azure File Sync agent version 4.0.1.0 or later is installed
2. Run the following PowerShell command on the server: `Reset-AzStorageSyncServerCertificate -ResourceGroupName <string> -StorageSyncServiceName <string>`
    
## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
