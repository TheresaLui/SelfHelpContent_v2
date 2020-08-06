<properties
pageTitle="Unable to delete storage resource due to disk(s) attached to a VM"
description="There are OS disk(s) in this storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_DiskAttached_OS"
diagnosticScenario="Unable to delete storage due to attached OS disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more OS disk(s) that are attached to a Classic VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more OS disk(s) that are attached to a Virtual Machine (VM). Please stop and delete the following VM(s) with attached OS disk before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: <br>

<!--$VMList-->[VMList]<!--/$VMList--> <br>

<!--/issueDescription-->
