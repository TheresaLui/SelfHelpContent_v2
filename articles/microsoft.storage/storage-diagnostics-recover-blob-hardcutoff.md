<properties
pageTitle="Deleted blob(s) are not recoverable"
description="Deleted blob(s) are not recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_blob_recovery_cannot_hardcutoff"
diagnosticScenario="Deleted blob(s) are not recoverable - Hard Cut Off"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Unable to recover blob(s) since all content was garbage collected

<!--issueDescription-->

Recovery of storage blob **{BlobPath}** in storage account **{ResourceName}** is not supported since all content was garbage-collected. We only support recovery of blobs which are deleted within **{HardCutOffDays}** days for {AccountType}. All contents that were deleted before {HardCutOffDays} would be garbage-collected.

<!--/issueDescription-->
As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These storage account(s) and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

# Recommended Steps
Enable [Soft Delete for blobs ](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview)on your storage account to ensure that accidentally deleted blobs can be recovered in the future.<br>

Soft delete for blobs protects your data from being accidentally or erroneously modified or deleted. When soft delete for blobs is enabled for a storage account, blobs, blob versions, and snapshots in that storage account may be recovered after they are deleted, within a retention period that you specify.


