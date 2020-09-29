<properties
pageTitle="Unable to delete or migrate storage resource due to disk(s) attached to a VM"
description="There are OS and data disks in this storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree, andyS210"
ms.author="passap, anye"
displayOrder=""
articleId="Storagev2insights_UnableToDeleteOrMigrate_DiskAttached"
diagnosticScenario="Unable to delete or migrate storage due to attached disks"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot <!--$AttemptedOperation-->[AttemptedOperation]<!--/$AttemptedOperation--> <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more disk(s) that are attached to a VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be <!--$AttemptedOperationPastTense-->[AttemptedOperationPastTense]<!--/$AttemptedOperationPastTense--> because it contains one or more disk(s) that are attached to a Virtual Machine (VM). 
<!--/issueDescription-->

## **Recommended Steps** 

In order to <!--$AttemptedOperation-->[AttemptedOperation]<!--/$AttemptedOperation--> the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first perform the following actions: <br>

1. [Delete the following VM(s) with attached OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk): <br>

<!--$VMList-->[VMList]<!--/$VMList--> <br>
<BR>

2. [Detach the following data disk(s) from its VM](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm): <br>

<!--$DataDiskWithVMList-->[DataDiskWithVMList]<!--/$DataDiskWithVMList--> <br>

