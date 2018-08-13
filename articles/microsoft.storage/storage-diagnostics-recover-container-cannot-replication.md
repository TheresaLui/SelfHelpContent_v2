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

# Unable to recover Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->**

<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover the Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->** that was deleted:<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo--><br>

 We use the geo-replicated copy of the Container for recovery and can only recover Container from GRS/RA-GRS Storage Accounts. Since the replication type of this Storage Account is **<!--$replicationType-->[replicationType]<!--/$replicationType-->**, recovery is not possible. 

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidently deleted content can be recovered in the future.
<!--/issueDescription-->
