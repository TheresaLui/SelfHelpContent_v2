<properties
pageTitle="Deleted blob is not recoverable without soft delete"
description="Deleted blob is not recoverable without soft delete"
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

# Unable to recover deleted blob because soft delete is not enabled

<!--issueDescription-->
We sincerely apologizes that we are unable to recover the deleted blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->**.<br>

We only support recovery of deleted blob(s) with soft delete. You can enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted Blobs will be recoverable in the future. 
<!--/issueDescription-->
