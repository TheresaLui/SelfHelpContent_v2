<properties
pageTitle="Storage Blob is recoverable with Soft Delete"
description="Deleted Storage Blob is recoverable with Soft Delete"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blob_recovery_softDelete_noDeletionTime"
diagnosticScenario="Storage Blob is recoverable with Soft Delete"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Deleted Storage Blob is recoverable within <!--$SoftDeleteRetenionDays-->[SoftDeleteRetenionDays]<!--/$SoftDeleteRetenionDays--> after deletion

<!--issueDescription-->
We have detected that [Soft Delete](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) is enabled in Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Deleted Storage Blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->** can be recovered within <!--$SoftDeleteRetenionDays-->[SoftDeleteRetenionDays]<!--/$SoftDeleteRetenionDays--> days after deletion. Please use [Undelete Blob API](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete#recovery) to perform recovery. 
<!--/issueDescription-->
