<properties
pageTitle="Cannot recover deleted storage account(s)"
description="Cannot recover deleted storage account(s)"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_recovery_cannot_GC"
diagnosticScenario="Deleted storage account(s) are not recoverable"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover storage account(s) because deleted account was already garbage collected

<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover the following deleted storage account(s): 

<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo--><br>
<!--/issueDescription-->
As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

