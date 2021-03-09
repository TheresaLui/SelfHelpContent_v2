<properties
pageTitle="Storage account(s) are not recoverable"
description="Storage account(s) are not recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_acct_recovery_cannot_hardcutoff"
diagnosticScenario="Storage account(s) are not recoverable - Hard Cut Off"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover storage account(s) because we only support recovery of accounts which are deleted within 14 days

<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover the following deleted storage account(s):

<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo--><br>

We are unable to recover accounts that have been deleted for more than 14 days, as they are garbage-collected.
<!--/issueDescription-->
As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

