<properties
pageTitle="FileSync older Agent Version"
description="One or more servers have an older version of the file sync agent installed"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_OlderAgentVersion"
diagnosticScenario="FileSync older Agent Version"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Older version of the Azure File Sync agent installed on server(s) under the Storage Sync Service

<!--issueDescription-->
The following servers registered under the Storage Sync Service **<!--$StorageSyncServiceName-->[StorageSyncServiceName]<!--/$StorageSyncServiceName-->** have an older version of the Azure File Sync agent installed. The agent should be updated to the latest version for these servers:

<!--$ServerNameList-->[ServerNameList]<!--/$ServerNameList-->.
<!--/issueDescription-->

## **Recommended steps**

[This document](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes) covers which versions of the Azure File Sync agent are supported as well as release notes for each agent. Note that older versions of the agent may have known bugs fixed in newer releases. Additionally, agent versions released before general availability will only function for a limited time period; please refer to the above article for the status of **different agent versions.**

## **Recommended Documents**

[Release notes for the Azure File Sync agent](https://docs.microsoft.com/azure/storage/files/storage-files-release-notes) 