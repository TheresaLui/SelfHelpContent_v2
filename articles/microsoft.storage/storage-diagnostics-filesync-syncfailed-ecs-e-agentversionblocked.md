<properties
pageTitle="Sync failed error - ECS_E_AGENT_VERSION_BLOCKED"
description="Sync failed error - ECS_E_AGENT_VERSION_BLOCKED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_AGENT_VERSION_BLOCKED"
diagnosticScenario="Sync failed error - ECS_E_AGENT_VERSION_BLOCKED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_AGENT_VERSION_BLOCKED

<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80C8306B or -2134364053**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs if the Azure File Sync agent version installed on the server is not supported.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, [upgrade](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#upgrade-paths) to a [supported agent version](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#supported-versions)

## **Recommended Documents**

- [Supported agent version](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#supported-versions)
- [Upgrade](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes#upgrade-paths)
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
