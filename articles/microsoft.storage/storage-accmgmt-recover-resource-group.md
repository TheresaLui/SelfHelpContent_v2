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
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="AA6F6A06-9039-4863-96EC-C20108131730"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Recover deleted resource group

## **Recommended Steps**

We can only attempt to recover deleted storage accounts within the resource group. All other resources will need to be manually rebuild. It is only possible to recover deleted storage accounts if both the following conditions are true:

1. Resource group was deleted in the last 14 days
2. A new storage account with the same name has not been created since

**Note:** As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This storage account and all its content may not be recoverable by Azure even when all conditions above are true.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

## **Recommended Documents**

* [Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)
