<properties
	pageTitle="Unable to delete Storage Account"
	description="Unable to delete Storage Account"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602694"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake"
/>

# Unable to delete Storage Account

## **Recommended steps**
### Deleting storage resource with Resource Manager (ARM) deployment:

- [Troubleshoot ARM storage resource deletion errors](https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors)

### Deleting storage account with classic deployment:

1. Go to [Azure Portal](https://portal.azure.com/) and select the Classic Storage Account you would like to delete.
2. Select **_Delete_** and a list of disks and images that prevents deletion will appear.
3. For each disk or image that prevents storage account deletion, delete the disk or image and retry deleting the storage account.
