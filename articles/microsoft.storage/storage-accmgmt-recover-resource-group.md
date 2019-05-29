<properties
	pageTitle="Recover deleted resource group"
	description="Recover deleted resource group troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32642177"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake"
	articleId="AA6F6A06-9039-4863-96EC-C20108131730"
/>

# Recover deleted resource group

## **Recommended steps**
We can only attempt to recover deleted storage accounts within the resource group. All other resources will need to be manually rebuild. It is only possible to recover deleted storage accounts if both the following conditions are true:

1. Resource group was deleted in the last 14 days<br> 
2. A new storage account with the same name has not been created since<br> 

**Note:** Garbage collection could occur on our system at any time, so we cannot guarantee successful recovery.

## **Recommended documents**
[Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)
