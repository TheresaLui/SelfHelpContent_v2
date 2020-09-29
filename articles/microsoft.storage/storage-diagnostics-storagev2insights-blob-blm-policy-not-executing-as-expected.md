<properties
pageTitle="Lifecycle Management may not have executed as expected"
description="Lifecycle Management may not have executed as expected"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storage_diagnostics_storagev2insights_blob_blm_policy_not_executing_as_expected"
diagnosticScenario="Lifecycle Management may not have executed as expected"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Lifecycle Management may not have executed as expected

<!--issueDescription-->
We have detected that Lifecycle Management couldn't affect some or any blobs due to the following reason(s):
<!--$displayMessage-->[displayMessage]<!--/$displayMessage-->
<!--/issueDescription-->

## **Recommended Steps**

For successful execution of Lifecycle Management policies on the storage account, refer the following execution and rule criteria to make modifications.

* New or updated policy - It could take from 24 to 48 hours for executing a new or updated policy. We recommend waiting up to 48 hours to see the first batch of data transition.
* Wildcard character '_*_' - This doesn't mean _'matches one or more occurrences of any character'_. The character '_*_' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '_*_' in the blob name.
* Wildcard character '?' - This doesn't mean _'match a single occurrence of any character'_. The character '?' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '?' in the blob name.
* prefixMatch with '!=' - The prefixMatch rules only consider positive(=) logical comparison. Therefore negative(!=) logical comparison are ignored.

## **Recommended Documents**

* [Naming and Referencing Blobs](https://docs.microsoft.com/rest/api/storageservices/naming-and-referencing-containers--blobs--and-metadata#blob-names)
* [Policy Rule Filters](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
* [Only Block Blob Type is currently supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
