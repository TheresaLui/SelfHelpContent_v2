<properties
pageTitle="Sync failed error - ECS_E_INCOMPATIBLE_FILTER_VERSION"
description="Sync failed error - ECS_E_INCOMPATIBLE_FILTER_VERSION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_INCOMPATIBLE_FILTER_VERSION"
diagnosticScenario="Sync failed error - ECS_E_INCOMPATIBLE_FILTER_VERSION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_INCOMPATIBLE_FILTER_VERSION
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80C80277 or -2134375817**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs because the Cloud Tiering filter driver (StorageSync.sys) version loaded is not compatible with the Storage Sync Agent (FileSyncSvc) service.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
If the Azure File Sync agent was upgraded, restart the server to complete the installation. If the error continues to occur, uninstall the agent, restart the server and reinstall the Azure File Sync agent.

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
