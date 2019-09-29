<properties
pageTitle="Access tiers is not supported on this storage account"
description="Access tiers is not supported on this storage account due to account type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="Storagev2insights_acct_type_tiering_notSupported"
diagnosticScenario="Access tiers is not supported on this storage account"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Access tiers is not supported on this storage account

<!--issueDescription-->
Storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> does not support access tiers as it is a <!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind--> account. Object storage data tiering to hot, cool, or archive is only supported in General Purpose v2 (GPv2) and Blob storage accounts and only available for block and append blobs.
* At account level - Only hot and cool access tiers can be set. The archive access tier is not available at the account level.
* At individual blob level 
  * Replication option LRS/GRS/RA-GRS   - All three access tiers hot,cool and archive can be set. 
  * Replication option ZRS/GZRS/RA-GZRS - Only hot and cool access tiers can be set.
<!--/issueDescription-->

## **Recommended Steps**
 Please change to a supported account type or replication option to use your preferred access tier. 

## **Recommended Documents**

* [Storage accounts that support tiering](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#storage-accounts-that-support-tiering)
* [Upgrade to a General-purpose v2 storage account](https://docs.microsoft.com/azure/storage/common/storage-account-upgrade)
* [Blob Storage Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#blob-storage-accounts)
* [General-purpose v2 Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts)
* Convert from ZRS to LRS/GRS - Live migration from ZRS to LRS, GRS or RA-GRS is not supported. You will need to manually move the data to a new or an existing storage account.
