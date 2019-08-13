<properties
pageTitle="Cannot recover Storage Blob Container"
description="Cannot recover Storage Blob Container"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blobContainer_recovery_cannot_replication"
diagnosticScenario="Storage Blob Container is not recoverable due to GC"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Unable to recover blob container(s) in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**

Microsoft Azure sincerely apologizes that we are unable to recover deleted blob container(s) in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. We use the geo-replicated copy of the blob container(s) for recovery and can only recover container(s) from GRS/RA-GRS storage accounts. Since the replication type of this Storage Account is **<!--$ReplicationType-->[ReplicationType]<!--/$ReplicationType-->**, recovery is not possible. 

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidently deleted content can be recovered in the future.
