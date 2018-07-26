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

# Unable to recover deleted Blob because Soft Delete is not enabled

<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover the deleted Storage Blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->**.<br>

We only support recovery of deleted Storage Blob(s) with Soft Delete. You can enable [Soft Delete for Azure Storage Blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted Blobs will be recoverable in the future. 
<!--/issueDescription-->
