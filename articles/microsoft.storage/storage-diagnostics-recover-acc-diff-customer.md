<properties
pageTitle="Storage account recovery"
description="Storage account recovery might be possible if the account with the same name can be deleted first"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_recovery_diffCustomer"
diagnosticScenario="Storage account recovery is not possible unless another account with the same name in another subscription can be deleted first"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage Account Recovery
<!--/issueDescription-->
Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** is not recoverable unless the account with the same name can be deleted first.
<!--/issueDescription-->

### 1. Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** recovered

We were able to successfully recover Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted: <!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo-->.

Microsoft may not always be able to recover your data. Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that your deleted data will be recoverable in the future. 

---

### 2. Unable to recover Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to garbage collection

Microsoft Azure sincerely apologizes that we are unable to recover the Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted:<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo-->.

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This Storage Account and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

--- 

### 3. Unable to recover Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to another account with the same name

We sincerely apologize that we are unable to recover the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted: <!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo-->.

A new storage account has already been created with the same name as the deleted account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. [Storage account names must be unique within Azure](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account#create-a-storage-account) so it is not possible to recover a storage account with the same name as an existing storage account. This storage account and all its content were cleaned up when the new storage account with the same name was created and are no longer recoverable by Azure.<br>

To ensure that accidentally deleted content can be recovered in the future, and to harden your applications against potential issues, refer to our recommended [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data).
