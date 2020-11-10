<properties
pageTitle="Unable to delete or migrate storage resource due to disk(s) attached to a VM"
description="There are OS disk(s) in this storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree, andyS210"
ms.author="passap, anye"
displayOrder=""
articleId="Storagev2insights_UnableToDeleteOrMigrate_DiskAttached_OS"
diagnosticScenario="Unable to delete delete or migrate storage due to attached OS disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot <!--$AttemptedOperation-->[AttemptedOperation]<!--/$AttemptedOperation--> <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more OS disk(s) that are attached to a Classic VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be <!--$AttemptedOperationPastTense-->[AttemptedOperationPastTense]<!--/$AttemptedOperationPastTense--> because it contains one or more OS disk(s) that are attached to a Virtual Machine (VM).
<!--/issueDescription-->

## **Recommended Steps**

* Please stop and delete the following VM(s) with attached OS disk before <!--$AttemptedOperationPresentParticiple-->[AttemptedOperationPresentParticiple]<!--/$AttemptedOperationPresentParticiple--> the <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->: <br>

<!--$VMList-->[VMList]<!--/$VMList--> <br>
