<properties
pageTitle="Access tiers is not supported on this blob type"
description="Access tiers is not supported on this blob type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storage_diagnostics_storagev2insights_blob_storage_access_tiers_blob_type_not_supported"
diagnosticScenario="Access tiers is not supported on this blob type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Access tiers is not supported on this blob type
<!--issueDescription-->
Specified blob does not support access tiers due to the following reason(s):

* <!--$displayMessage-->[displayMessage]<!--/$displayMessage--> 
 
<!--/issueDescription-->

## **Recommended Steps**

* Storage data tiering to hot, cool, or archive is only available for block blobs
* Block blob with lease - The lease needs to be broken first before changing the access tier
* Page blob - These can't be moved to a different tier
* Append blob - These can't be moved to a different tier  

## **Recommended Documents**

 * [Storage accounts that support tiering](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#storage-accounts-that-support-tiering)
 * [Blob Lease](https://docs.microsoft.com/rest/api/storageservices/lease-blob#request-headers)
 
