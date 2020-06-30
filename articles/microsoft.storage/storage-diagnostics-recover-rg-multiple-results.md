<properties
pageTitle="Resource Group recovery results"
description="Resource Group recovery results"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_rg_recovery_results"
diagnosticScenario="Storage account recovery with multiple results"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# <!--issueDescription-->Recover storage account(s) in deleted Resource Group<!--/issueDescription-->

Microsoft Azure team completed storage account recovery process in Resource Group **<!--$ResourceGroupName-->[ResourceGroupName]<!--/$ResourceGroupName-->** that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->** with the following results:

### Successfully recovered storage account(s):
We were able to successfully recover the following storage account(s). Please check and confirm if you can access them:

**_[Enter list of accounts where recovery succeeded]_**

### Unable to recover storage account(s):
Unfortunately, our recovery attempt was not successful for the following storage account(s) since all its data has already been cleaned up after deletion. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) were cleaned up after deletion and are no longer recoverable by Azure:

**_[Enter list of accounts which could NOT be recovered]_**

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

