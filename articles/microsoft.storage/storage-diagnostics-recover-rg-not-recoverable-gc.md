<properties
pageTitle="Cannot recover deleted Resource Group"
description="Cannot recover storage account within deleted Resource Group"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_rg_recovery_cannot_GC"
diagnosticScenario="Resource Group recovery - unable to recover"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover deleted Resource Group
<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover **<!--$ResourceGroupName-->[ResourceGroupName]<!--/$ResourceGroupName-->** Resource Group that was deleted on **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->**.
<!--/issueDescription-->

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. The deleted Resource Group and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.
