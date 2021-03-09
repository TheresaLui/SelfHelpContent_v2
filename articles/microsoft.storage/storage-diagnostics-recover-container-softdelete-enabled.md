<properties
pageTitle="Blob container recovery with soft delete enabled"
description="Blob container recovery with soft delete enabled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_container_recovery_softdelete_enabled"
diagnosticScenario="Blob container recovery with soft delete enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Blob Recovery with Soft Delete disabled

<!--issueDescription-->

The deleted blob container(s) could be recoverable because container soft delete is enabled on storage account **{ResourceName}**. The container can be recovered if soft delete was enabled when deletion happened and if the recovery operation is completed within **{SoftDeleteRetentionDays}** days after deletion."

<!--/issueDescription-->
## Recommended Steps
To recover your deleted container(s), follow these [steps](https://docs.microsoft.com/azure/storage/blobs/soft-delete-container-overview?tabs=powershell)
