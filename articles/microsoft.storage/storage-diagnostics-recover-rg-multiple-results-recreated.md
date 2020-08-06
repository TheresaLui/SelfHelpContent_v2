<properties
pageTitle="Resource Group recovery with recreated storage accounts"
description="Resource Group recovery with recreated storage accounts"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_rg_recovery_maybe_wSameName"
diagnosticScenario="Storage account recovery with multiple results"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Resource group recover

## Another account with the same name must be deleted before recovery

<!--issueDescription-->
Microsoft Azure team cannot recover deleted storage account(s) in Resource Group **<!--$ResourceGroupName-->[ResourceGroupName]<!--/$ResourceGroupName-->** that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->** because another account with the same name has since been created<!--/issueDescription-->:

<!--$DeletionInfo_Recreated-->[DeletionInfo_Recreated]<!--/$DeletionInfo_Recreated-->

<!--/issueDescription-->

[Storage account names must be unique within Azure](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account#create-a-storage-account) so it is not possible to recover deleted storage accounts with the same name as another live account in Azure. If you are the owner of these new storage accounts, you will need to delete the new accounts before we can attempt recovery of the deleted ones. Our recovery attempt is based on best effort and we cannot guarantee that it will succeed. Please backup your data in the new storage account before deletion.

---
## Storage account recovery results

Microsoft Azure team completed storage account recovery process in Resource Group **<!--$ResourceGroupName-->[ResourceGroupName]<!--/$ResourceGroupName-->** that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->** with the following results:

### Successfully recovered storage account(s):
We were able to successfully recover the following storage account(s). Please check and confirm if you can access them:

**_[Enter list of accounts where recovery succeeded]_**

### Unable to recover storage account(s):
Unfortunately, our recovery attempt was not successful for the following storage account(s) since all its data has already been cleaned up after deletion. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) were cleaned up after deletion and are no longer recoverable by Azure:

**_[Enter list of accounts which could NOT be recovered]_**

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

