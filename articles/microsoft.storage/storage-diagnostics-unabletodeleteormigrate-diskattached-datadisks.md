<properties
pageTitle="Unable to delete or migrate storage resource due to disk(s) attached to a VM"
description="There are data disk(s) in the storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree, andyS210"
ms.author="passap, anye"
displayOrder=""
articleId="Storagev2insights_UnableToDeleteOrMigrate_DiskAttached_Data"
diagnosticScenario="Unable to delete or migrate storage due to attached data disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot <!--$AttemptedOperation-->[AttemptedOperation]<!--/$AttemptedOperation--> <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more data disk(s) that are attached to a VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be <!--$AttemptedOperationPastTense-->[AttemptedOperationPastTense]<!--/$AttemptedOperationPastTense--> because it contains one or more data disk(s) that are attached to a Virtual Machine (VM).
<!--/issueDescription-->

## **Recommended Steps** 

* Please [detach the following data disk(s) from its VM](https://docs.microsoft.com/azure/lab-services/devtest-lab-attach-detach-data-disk#detach-a-data-disk) before <!--$AttemptedOperationPresentParticiple-->[AttemptedOperationPresentParticiple]<!--/$AttemptedOperationPresentParticiple--> the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->:

<!--$DataDiskWithVMList-->[DataDiskWithVMList]<!--/$DataDiskWithVMList-->

