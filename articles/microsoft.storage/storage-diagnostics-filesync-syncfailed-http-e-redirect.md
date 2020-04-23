<properties
pageTitle="Sync failed error - HTTP_E_STATUS_REDIRECT_KEEP_VERB"
description="Sync failed error - HTTP_E_STATUS_REDIRECT_KEEP_VERB"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_HTTP_E_STATUS_REDIRECT_KEEP_VERB"
diagnosticScenario="Sync failed error - HTTP_E_STATUS_REDIRECT_KEEP_VERB"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>


# Azure File Sync failed error - HTTP_E_STATUS_REDIRECT_KEEP_VERB

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80190133 or -2145844941**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because Azure File Sync does not support HTTP redirection (3xx status code).<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, disable HTTP redirect on your proxy server or network device.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)


