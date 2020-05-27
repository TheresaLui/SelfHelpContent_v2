<properties
pageTitle="Deleted blob is not recoverable without soft delete"
description="Deleted blob is not recoverable without soft delete"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blob_recovery_noSoftDelete"
diagnosticScenario="Blob is not recoverable without soft delete"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover deleted blob because soft delete is not enabled

<!--issueDescription-->
We sincerely apologize that we are unable to recover the deleted blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->**.

Azure Storage now offers soft delete for blob objects so that you can more easily recover your data when it is erroneously deleted by an application or other storage account user.<!--/issueDescription--> You can enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted blobs will be recoverable in the future. 

