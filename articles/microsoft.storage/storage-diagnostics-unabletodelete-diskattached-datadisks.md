<properties
pageTitle="Unable to delete storage resource due to disk(s) attached to a VM"
description="There are data disk(s) in the storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_DiskAttached_Data"
diagnosticScenario="Unable to delete storage due to attached data disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more data disk(s) that are attached to a VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> cannot be deleted because it contains one or more data disk(s) that are attached to a Virtual Machine (VM):

<!--$DataDiskWithVMList-->[DataDiskWithVMList]<!--/$DataDiskWithVMList-->
<!--/issueDescription-->

 Please [detach the following data disk(s) from its VM](https://docs.microsoft.com/azure/lab-services/devtest-lab-attach-detach-data-disk#detach-a-data-disk) before deleting the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->.
