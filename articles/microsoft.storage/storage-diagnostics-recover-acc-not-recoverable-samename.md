<properties
pageTitle="Cannot recover storage account"
description="Cannot recover storage account due to another active account with the same name"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_recovery_cannot_sameName"
diagnosticScenario="Storage account is not recoverable due to another active account with the same name"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**

<!--issueDescription-->
We sincerely apologize that we are unable to recover the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that was deleted:<!--$DeletionInfo-->[DeletionInfo]<!--/$DeletionInfo-->

A new storage account has already been created with the same name as the deleted account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**.<!--/issueDescription--> [Storage account names must be unique within Azure](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account#create-a-storage-account) so it is not possible to recover a storage account with the same name as an existing storage account. This storage account and all its content were cleaned up when the new storage account with the same name was created and are no longer recoverable by Azure.<br>

To ensure that accidentally deleted content can be recovered in the future, and to harden your applications against potential issues, please refer to our recommended [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data).
