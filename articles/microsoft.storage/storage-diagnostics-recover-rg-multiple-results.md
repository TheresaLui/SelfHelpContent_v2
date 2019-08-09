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
cloudEnvironments="public"
/>

# Resource group recovery

Microsoft Azure team completed storage account(s) recovery process in Resource Group **<!--$ResourceGroupName-->[ResourceGroupName]<!--/$ResourceGroupName-->** that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->** with the following results:

### Successfully recovered storage acount(s):
**_[Enter list of accounts where recovery succeeded]_**

Please check and confirm if you can access storage account(s) above. 

### Unable to recover storage account(s):
**_[Enter list of accounts which could NOT be recovered]_**

Unfortunately, our recovery attempt was not successful for storage account(s) above since all its data has already been cleaned up after deletion. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. Contents in storage accounts in the deleted Resource Group was cleaned up after deletion and is no longer recoverable by Azure.

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

