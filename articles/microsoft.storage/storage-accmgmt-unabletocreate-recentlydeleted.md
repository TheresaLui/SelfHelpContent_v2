<properties
	pageTitle="Unable to re-create storage account"
	description="Unable to create storage account with the same name as recently deleted account"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
    ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639220"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="9603FCBD-3B97-406B-9348-BCD4A5DC374E"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Unable to create storage account with the same name as recently deleted account

Azure storage requires that [storage account names must be unique](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors#cause), so a new storage account with the same name cannot be created until after the old account has been cleaned up in the backend. You can either create a new storage account with a different name now or retry account creation with the same name at a later time. It can take up to 14 days after deletion of the previous account for the backend cleanup to completed. 

## **Recommended Documents**
- [Storage account name must be unique](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors#cause)
