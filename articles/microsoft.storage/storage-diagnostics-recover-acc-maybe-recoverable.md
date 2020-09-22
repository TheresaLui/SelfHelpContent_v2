<properties
pageTitle="Deleted storage account(s) might be recoverable"
description="Deleted storage account(s) might be recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_recovery_maybe"
diagnosticScenario="Deleted storage account(s) might be recoverable"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage Account Recovery
<!--issueDescription-->
Deleted storage accounts might be recoverable.
<!--/issueDescription-->

### 1. Storage account(s) recovery successful

We were able to successfully recover the following deleted storage account(s): 

**[Deleted storage account name(s)]**

Microsoft may not always be able to recover your data. Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that your deleted data will be recoverable in the future. 

---

### 2. Unable to recover storage account(s) because deleted account was already garbage collected

Microsoft sincerely apologizes that we are unable to recover the following deleted storage account(s): 

**[Deleted storage account name(s)]**

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This Storage Account and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.
