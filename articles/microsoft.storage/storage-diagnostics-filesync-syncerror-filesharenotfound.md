<properties
pageTitle="Sync error - file share not found"
description="Sync error - file share not found"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_FileShareNotFound"
diagnosticScenario="Sync error - file share not found"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->  : File Share not found.

<!--issueDescription-->
Azure File Sync failed with error **<!--$ErrorString-->[ErrorString]<!--/$ErrorString-->** on Server Endpoint **<!--$ServerEndpointName-->[ServerEndpointName]<!--/$ServerEndpointName-->**.
<!--/issueDescription-->

## **Recommended Steps**

1. Make sure the Azure File Share  **<!--$ShareName-->[ShareName]<!--/$ShareName-->** still exists
2. If the Azure File Share was deleted, create a new File Share and then recreate the Sync Group
3. First delete the Server Endpoint and then the Cloud Endpoint within the existing Sync Group
4. Then add the new File Share as the Cloud Endpoint and the same server as the Server Endpoint

Note that when you delete a File Share, you delete Azure File Sync metadata, so even if you create another File Share with the same name, you cannot just reattach it to the Sync Group as the Sync metadata will have been lost.

