<properties
pageTitle="Unable to delete storage resource due to detached classic disk(s)"
description="There are detached classic disk(s) in this storage resource that prevents deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_DiskDetached_Classic"
diagnosticScenario="Unable to delete storage due to detached classic disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more classic disk(s)

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more unattached classic disk(s). Although the following disk(s) are not currently attached to a VM, it still prevents deletion of storage account <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->.
<!--/issueDescription-->

## **Recommended Steps**

In order to delete the storage account, you must first delete the following disk(s):<br>

<!--$DiskList-->[DiskList]<!--/$DiskList-->

Alternatively, these disks can be deleted during storage account deletion using [Azure Portal](https://portal.azure.com) with the _'Automatically delete unattached disks and images'_ option selected.

## **Recommended Documents**

* [Unmanaged disks: Find and delete unattached disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks#unmanaged-disks-find-and-delete-unattached-disks)
* [Errors when deleting classic storage resources](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/storage-classic-cannot-delete-storage-account-container-vhd#unable-to-delete-storage-account)
