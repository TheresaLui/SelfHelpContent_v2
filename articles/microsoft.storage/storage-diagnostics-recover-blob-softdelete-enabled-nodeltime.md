<properties
pageTitle="Deleted blob is recoverable with Soft Delete"
description="Deleted blob is recoverable with Soft Delete"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blob_recovery_softDelete_noDeletionTime"
diagnosticScenario="Storage Blob is recoverable with Soft Delete"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Deleted blob can be recovered within <!--$SoftDeleteRetenionDays-->[SoftDeleteRetenionDays]<!--/$SoftDeleteRetenionDays--> days after deletion

<!--issueDescription-->
The deleted storage blob **<!--$BlobPath-->[BlobPath]<!--/$BlobPath-->** is recoverable within <!--$SoftDeleteRetentionDays-->[SoftDeleteRetentionDays]<!--/$SoftDeleteRetentionDays--> days after deletion<!--/issueDescription--> because soft delete is enabled for the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. 
<!--/issueDescription-->

## **Recommended Steps**

* Use the [Undelete Blob API](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete#recovery) to perform recovery

## **Recommended Documents**

*  [Soft Delete](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)
