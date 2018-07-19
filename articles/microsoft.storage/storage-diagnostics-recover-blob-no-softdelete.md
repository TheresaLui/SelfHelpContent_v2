<properties
pageTitle="Blob is not recoverable without soft delete"
description="Blob is not recoverable without soft delete"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blob_recovery_noSoftDelete"
diagnosticScenario="Blob is not recoverable without soft delete"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Unable to recover blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->** because Soft Delete is disabled
We do not support recovery of deleted Storage Blob without soft delete. You can enable [soft delete for Azure Storage Blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted Blobs will be recoverable in the future. 

