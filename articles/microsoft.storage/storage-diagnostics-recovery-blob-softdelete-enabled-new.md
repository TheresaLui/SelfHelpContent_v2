<properties
pageTitle="Blob Recovery with soft delete enabled"
description="Blob Recovery with soft delete enabled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_blob_recovery_softdelete_enabled_new"
diagnosticScenario="Blob Recovery with soft delete disabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Blob Recovery with Soft Delete enabled
<!--issueDescription-->

The deleted blob could be recoverable because blob soft delete is enabled on storage account **{ResourceName}**. The blob can be recovered if soft delete was enabled when deletion happened and the recovery operation is completed within **{SoftDeleteRetentionDays}** days after deletion.

<!--/issueDescription-->

## Recommended Steps
To recover your deleted blobs, follow these [steps.](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview#recovery)