<properties
pageTitle="Sync failed error - ECS_E_AUTH_SRV_CERT_NOT_FOUND"
description="Sync failed error - ECS_E_AUTH_SRV_CERT_NOT_FOUND"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_AUTH_SRV_CERT_NOT_FOUND"
diagnosticScenario="Sync failed error - ECS_E_AUTH_SRV_CERT_NOT_FOUND"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error -ECS_E_AUTH_SRV_CERT_NOT_FOUND
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80228 or -2134375896**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the certificate used for authentication is not found.<br/><br/>
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, perform the following steps:

1. Verify Azure File Sync agent version 4.0.1.0 or later is installed
2. Run the following PowerShell command on the server: `Reset-AzStorageSyncServerCertificate -ResourceGroupName <string> -StorageSyncServiceName <string>`

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
