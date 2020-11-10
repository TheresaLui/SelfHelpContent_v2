<properties
pageTitle="Unable to delete storage resource due to scope lock"
description="There are scope lock(s) in this storage resource that prevents deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_ScopeLocked"
diagnosticScenario="Unable to delete storage due to scope lock"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to lock(s) to prevent unexpected changes

<!--issueDescription-->

The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> cannot be deleted because it contains one or more lock(s) to prevent unexpected changes. Please remove the following lock(s) before deleting <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> <!--$ResourceName-->[ResourceName]<!--/$ResourceName-->:

<!--$ScopeLockTable-->[ScopeLockTable]<!--/$ScopeLockTable-->
<!--/issueDescription-->

## **Recommended Documents**

* [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)

