<properties
pageTitle="Sync error - cannot access external storage account"
description="Sync error - cannot access external storage account"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_CannotAccessExternalStorageAccount"
diagnosticScenario="Sync error - cannot access external storage account"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->  : Sync cannot access the Azure File Share specified in the Cloud Endpoint.

<!--issueDescription-->
Azure File Sync failed on Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->** because it cannot access the Azure File Share  **<!--$ShareName-->[ShareName]<!--/$ShareName-->**.<br>
<!--/issueDescription-->

## **Recommended Steps**

1. Verify the Azure File Share still exists.<br>
2. Ensure the Azure subscription containing the File Share is not suspended.<br>
3. Ensure access from all networks to the Storage Account is allowed. Azure File Sync does not yet support [Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/files/storage-sync-files-firewall-and-proxy) for a Storage Account. You can check the configuration in the Azure Portal by going to the Storage Account and then clicking on the 'Firewalls and Virtual Networks' tab.<br>
4. In the Azure portal under the Storage Account, go to the 'Access Control (IAM)' tab and verify the Storage Sync Service role has access to the Storage Account. The scope for 'Hybrid File Sync Service' must be set to 'This Resource'.

