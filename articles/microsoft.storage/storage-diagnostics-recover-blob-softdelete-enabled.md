<properties
pageTitle="Storage Blob recovery is not supported"
description="Storage Blob recovery is not supported"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blob_recovery_softDelete"
diagnosticScenario="Account cannot be created because deleted account with the same name has not been GC"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Deleted Storage Blob is recoverable until **<!--$RecoveryTime-->[RecoveryTime]<!--/$RecoveryTime-->**

<!--issueDescription-->
We have detected that [Soft Delete](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) is enabled in Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Deleted Storage Blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->** is recoverable with Soft Delete until **<!--$RecoveryTime-->[RecoveryTime]<!--/$RecoveryTime-->**. Please use [Undelete Blob API](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete#recovery) to perform recovery. 
<!--/issueDescription-->
