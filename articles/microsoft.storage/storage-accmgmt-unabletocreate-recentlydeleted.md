<properties
	pageTitle="Unable to create storage account with the same name as deleted account"
	description="Unable to create storage account with the same name as deleted account"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
    ms.authors="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639220"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake"
	articleId="9603FCBD-3B97-406B-9348-BCD4A5DC374E"
/>

# Unable to create storage account with the same name as recently deleted account

Azure storage requires that [storage account name must be unique](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors#cause), so a new storage account with the same name cannot be created until after the old account has been cleaned up in the backend. You can either create a new storage account with a different name now or retry account creation with the same name 14 days after deletion of the previous account. 

## **Recommended Documents**
- [Storage account name must be unique](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors#cause)
