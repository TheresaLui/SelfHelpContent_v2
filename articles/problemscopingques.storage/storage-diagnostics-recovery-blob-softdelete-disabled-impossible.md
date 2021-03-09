<properties
pageTitle="Blob Recovery with soft delete disabled"
description="Blob Recovery with soft delete disabled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_blob_recovery_cannot_softdelete_disabled"
diagnosticScenario="Blob Recovery with soft delete disabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Blob Recovery with Soft Delete disabled

<!--issueDescription-->

Client side recovery of storage blob **{BlobPath}** is not supported because soft delete is disabled on storage account **{ResourceName}**. Manual recovery from server side is also not possible. We have run the backend check and find that some data has been permanently lost, so the data cannot be recovered.

<!--/issueDescription-->
As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

## Recommended Steps
Enable [Soft Delete for blobs ](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview)on your storage account to ensure that accidentally deleted blobs can be recovered in the future.<br>

Soft delete for blobs protects your data from being accidentally or erroneously modified or deleted. When soft delete for blobs is enabled for a storage account, blobs, blob versions, and snapshots in that storage account may be recovered after they are deleted, within a retention period that you specify.