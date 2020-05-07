<properties
pageTitle="Sync failed to recall - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
description="Sync failed to recall - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedToRecall_ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
diagnosticScenario="Sync failed to recall - ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed to recall file(s) due to error **ECS_E_EXTERNAL_STORAGE_ACCOUNT_AUTHORIZATION_FAILED**

<!--issueDescription-->
Azure File Sync failed to recall file(s) for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c8305f or -2134364065**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs due to authorization failure to the storage account.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, Ensure Azure File Sync has access to the storage account by performing the following steps in Azure portal:

1. Click **Access control (IAM)** on the left-hand table of contents
1. Click the **Role assignments** tab to the list the users and applications (*service principals*) that have access to your storage account
1. Verify **Hybrid File Sync Service** appears in the list with the **Reader and Data Access** role

	If **Hybrid File Sync Service** does not appear in the list, perform the following steps:

	- Click **Add**
	- In the **Role** field, select **Reader and Data Access**
	- In the **Select** field, type **Hybrid File Sync Service**, select the role and click **Save**

## **Recommended Documents**

- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)
- [Azure File Sync has access to the storage account](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#troubleshoot-rbac)
