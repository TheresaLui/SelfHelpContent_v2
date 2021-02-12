<properties
pageTitle="Rehydrated blobs from archive access tier will automatically get transitioned  back to archive tier due to Lifecycle Management Policy"
description="Rehydrated blobs from archive access tier will automatically get transitioned  back to archive tier due to Lifecycle Management Policy"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storage_diagnostics_storagev2insights_blob_storage_access_tiers_rehyrated_blob_conflict_blm_policy"
diagnosticScenario="Blob rehyration potential conflict with BLM policy"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Rehydrated blobs from archive access tier will automatically get transitioned back to archive tier due to Lifecycle Management Policy set on storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName-->"

<!--issueDescription-->
Rehydrated blobs from archive access tier will automatically get transitioned back to archive tier due to Lifecycle Management Policy set on storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName-->. Below are the potential rehydration conflicts with the rule filters set in the current policy.

<!--$displayMessage-->[displayMessage]<!--/$displayMessage-->

<!--/issueDescription-->

## **Recommended Steps**

You can take one of more of these steps to overcome the conflict and prevent the rehydrated blob getting transitioned back to archive access tier.

* Modify the Rule Filters or Actions in the Lifecycle Management Policy on the storage account.
* Disable the Lifecycle Management Policy on the storage account.
* Copy an archived blob to an online tier in another storage account or a different container in same storage account. Make sure the other container is not covered by the policy.

## **Recommended Documents**

 * [Rule Filters and Actions in the Lifecycle Management Policy](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
 * [Copy an archived blob to an online tier](https://docs.microsoft.com/azure/storage/blobs/storage-blob-rehydration#copy-an-archived-blob-to-an-online-tier)
