<properties
pageTitle="Cannot recover storage account"
description="Cannot recover storage account"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_acct_recovery_maybe"
diagnosticScenario="Storage account is not recoverable due to GC"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** may be recoverable

<!--issueDescription-->
## Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** recovered

We were able to successfully recover storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted:<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo--><br>

Microsoft may not always be able  to recover your data. You can follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that your deleted data will be recoverable in the future. 

---

## Unable to recover storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**

Microsoft sincerely apologizes that we are unable to recover the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted:<br>
<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo--><br>

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This storage account and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidently deleted content can be recovered in the future.
<!--/issueDescription-->
