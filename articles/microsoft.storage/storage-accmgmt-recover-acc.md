<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="Passaree"
    ms.author="passap"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32602701,32642178,32688873"
    resourceTags="recovery"
    productPesIds="15629,16459"
    cloudEnvironments="public, blackForest, fairfax, mooncake"
    articleId="e6c363fc-ee76-4afb-8278-bbb74b17051e"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Recover deleted storage account

Most users can determine if it might be possible to recover their deleted storage account using the steps below.

## **Recommended Steps**

Storage account recovery is only possible if both the following conditions are true:

1. The storage account was deleted in the last 14 days
2. A new storage account with the same name has not been created since

**Note:** It may not be possible to recover deleted storage account even if above conditions are true. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This storage account and all its content may not be recoverable by Azure even when all conditions above are true.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

## **Recommended Documents**

* [Best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data)<br>
* [How to recover a deleted storage account](https://docs.microsoft.com/azure/storage/files/storage-how-to-recover-deleted-account)
