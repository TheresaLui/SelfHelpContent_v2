<properties
pageTitle="Unable to delete storage resource due to snapshot(s)"
description="There are snapshot(s) in this storage resource that prevents deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete-Snapshots"
diagnosticScenario="Unable to delete storage due to snapshot(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more snapshot(s)

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more snapshot(s):

<!--$SnapshotList-->[SnapshotList]<!--/$SnapshotList-->

<!--/issueDescription-->

In order to delete the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first [delete the snapshot(s) listed above](https://docs.microsoft.com/azure/storage/blobs/storage-blob-snapshots#delete-snapshots).
