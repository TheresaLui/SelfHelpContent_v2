<properties
pageTitle="Deleted blob recovery is not supported"
description="Deleted blob recovery is not supported"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blob_recovery_softDelete"
diagnosticScenario="Account cannot be created because deleted account with the same name has not been GC"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Deleted blob is recoverable until **<!--$RecoveryTime-->[RecoveryTime]<!--/$RecoveryTime-->**

<!--issueDescription-->
The storage blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->** that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->** is recoverable because soft delete is enabled for the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. The blob can be recovered if the recovery operation is completed before **<!--$RecoveryTime-->[RecoveryTime]<!--/$RecoveryTime-->**.
<!--/issueDescription-->

Please use the [Undelete Blob API](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete#recovery) to perform recovery. 
