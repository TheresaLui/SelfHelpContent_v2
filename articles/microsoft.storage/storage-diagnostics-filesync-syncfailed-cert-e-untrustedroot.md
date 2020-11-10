<properties
pageTitle="Sync failed error - CERT_E_UNTRUSTEDROOT"
description="Sync failed error - CERT_E_UNTRUSTEDROOT"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_CERT_E_UNTRUSTEDROOT"
diagnosticScenario="Sync failed error - CERT_E_UNTRUSTEDROOT"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - CERT_E_UNTRUSTEDROOT

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to error **The server failed to establish a secure connection. The cloud service received an unexpected certificate (error code 0x800b0109 or -2146762487)**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.

This error can happen if your organization is using an SSL terminating proxy or if a malicious entity is intercepting the traffic between your server and the Azure File Sync service.

If you are certain that this is expected (because your organization is using an SSL terminating proxy), you skip certificate verification with a registry override. 
<!--/issueDescription-->

## **Recommended steps**

1. Create the SkipVerifyingPinnedRootCertificate registry value

    ```powershell
    New-ItemProperty -Path HKLM:\SOFTWARE\Microsoft\Azure\StorageSync -Name SkipVerifyingPinnedRootCertificate -PropertyType DWORD -Value 1
    ```

2. Restart the sync service on the registered server

    ```powershell
    Restart-Service -Name FileSyncSvc -Force
    ```

By setting this registry value, the Azure File Sync agent will accept any locally trusted SSL certificate when transferring data between the server and the cloud service.


## **Recommended Documents**
[Troubleshoot sync error - CERT_E_UNTRUSTEDROOT (error code 0x800b0109 or -2146762487)](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2146762487)