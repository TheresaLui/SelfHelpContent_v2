<properties
pageTitle="Unable to delete storage resource due to disk(s) attached to a VM"
description="There are OS and data disks in this storage resource that is attached to a VM"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_DiskAttached"
diagnosticScenario="Unable to delete storage due to attached disks"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more disk(s) that are attached to a VM

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more disk(s) that are attached to a Virtual Machine (VM).
<!--/issueDescription-->

## **Recommended Steps**

In order to delete the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first perform the following actions:

1. [Delete the following VM(s) with attached OS disk](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk):

  <!--$VMList-->[VMList]<!--/$VMList-->

2. [Detach the following data disk(s) from its VM](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm):

  <!--$DataDiskWithVMList-->[DataDiskWithVMList]<!--/$DataDiskWithVMList-->
