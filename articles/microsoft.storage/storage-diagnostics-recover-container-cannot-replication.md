<properties
pageTitle="Cannot recover storage blob container due to account replication type"
description="Storage blob container is not recoverable due to storage account replication type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blobContainer_recovery_cannot_replication"
diagnosticScenario="Storage blob container is not recoverable due to storage account replication type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover blob container(s) in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to its replication type

<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover deleted blob container(s) in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. We use the geo-replicated copy of the blob container(s) for recovery and can only recover container(s) from GRS or RA-GRS storage accounts. Since the replication type of this storage account is **<!--$ReplicationType-->[ReplicationType]<!--/$ReplicationType-->**, recovery is not possible. 
<!--/issueDescription-->

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.
