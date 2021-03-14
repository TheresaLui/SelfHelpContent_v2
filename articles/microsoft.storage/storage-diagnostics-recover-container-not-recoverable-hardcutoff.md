<properties
pageTitle="Deleted blob containers are not recoverable"
description="Deleted blob containers are not recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_container_recovery_cannot_hardcutoff"
diagnosticScenario="Deleted blob containers are not recoverable - Hard Cut Off"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Blob Container cannot be recovered

<!--issueDescription-->

Unable to recover blob container(s) that was deleted in storage account **{ResourceName}** on {DeletionTime}. We only support recovery of container(s) which are deleted within 14 days."

<!--/issueDescription-->
## Recommended Steps
Enable [Soft Delete for containers ](https://docs.microsoft.com/azure/storage/blobs/soft-delete-container-overview?tabs=powershell)on your storage account to ensure that accidentally deleted containers can be recovered in the future.<br>

Soft delete for containers protects your data from being accidentally or maliciously deleted. When container soft delete is enabled for a storage account, any deleted container and their contents are retained in Azure Storage for the period that you specify. During the retention period, you can restore previously deleted containers. Restoring a container restores any blobs within that container when it was deleted.