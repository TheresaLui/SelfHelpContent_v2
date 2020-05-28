<properties
	pageTitle="Unable to delete Storage Account"
	description="Unable to delete Storage Account"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602694,32639219"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="24a774b4-3aaf-46b5-aa55-64247af90249"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Unable to delete Storage Resource

## **Recommended Documents**

### **Deleting storage resource with classic deployment**

Disks and images that were previously attached to a VM can prevent deletion of storage resources **even if the disk is no longer attached or the VM is already deleted**. Please follow the instruction below if you are trying to delete classic storage resources:
- [Troubleshoot classic storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/storage-classic-cannot-delete-storage-account-container-vhd)

### **Deleting storage resource with Resource Manager (ARM) deployment**

- [Troubleshoot ARM storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors)

### **Lock resource**

Administrator, may need lock a subscription, resource group, or resource to prevent accidental deletion or modification. 

- [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources)
- [I am unable to remove the lock on resources](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources#who-can-create-or-delete-locks)
