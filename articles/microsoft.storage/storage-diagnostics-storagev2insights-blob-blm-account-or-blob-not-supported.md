<properties
pageTitle="Lifecycle Management couldn't transition blobs due to unsupported account or blob type"
description="Lifecycle Management couldn't transition blobs due to unsupported account or blob type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_blm_account_or_blob_not_supported"
diagnosticScenario="Lifecycle Management couldn't transition blobs due to unsupported account or blob type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Lifecycle Management couldn't transition blobs due to unsupported account or blob type

<!--issueDescription-->
We have detected that Lifecycle Management couldn't affect some or any blobs due to the following reason:

<!--$displayMessage-->[displayMessage]<!--/$displayMessage-->

<!--/issueDescription-->

## **Recommended Steps**

* For successful execution of Lifecycle Management policies on the storage account, identify your issue in the description above, and then refer to the appropriate article in the following list.

## **Recommended Documents**

 * [Storage account types supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#storage-account-support)
 * [Only Block and Append Blob Types are currently supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule)
 * [Lease Blob locks a blob for write or delete operation hence is not affected by Lifecycle Management](https://docs.microsoft.com/rest/api/storageservices/lease-blob)
