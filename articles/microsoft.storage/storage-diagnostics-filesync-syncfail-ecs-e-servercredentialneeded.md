<properties
    pageTitle="Sync failed error - ECS_E_SERVER_CREDENTIAL_NEEDED "
    description="Sync failed error - ECS_E_SERVER_CREDENTIAL_NEEDED"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="passaree"
    ms.author="passap"
    displayOrder=""
    articleId="FileSync_FailedError_ECS_E_SERVER_CREDENTIAL_NEEDED"
    diagnosticScenario="Sync failed error - ECS_E_SERVER_CREDENTIAL_NEEDED"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure File Sync failed error - ECS_E_SERVER_CREDENTIAL_NEEDED 
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code: 0x80c80300 or -2134375680**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error typically occurs because the server time is incorrect.<br/><br/>
<!--/issueDescription-->

## **Recommended Steps**
Verify the server time is correct. If the server is running in a virtual machine, verify the time on the virtual host is correct.

## **Recommended Documents**
- [Troubleshoot Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134347507)

