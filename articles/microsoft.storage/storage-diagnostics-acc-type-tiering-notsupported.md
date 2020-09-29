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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Access tiers is not supported on this storage account

<!--issueDescription-->
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** does not support access tiers as it is a **<!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind-->** account. 
<!--/issueDescription-->

## **Recommended Steps**

Storage data tiering to hot, cool, or archive is only supported in General Purpose v2 (GPv2) and Blob storage accounts and only available for block blobs. 

Convert from ZRS to LRS/GRS - Live migration from ZRS to LRS, GRS or RA-GRS is not supported. You will need to manually move the data to a new or an existing storage account.

### Account level settings

* Only hot and cool access tiers can be set. The archive access tier is not available at the account level.
* Account Redundancy – LRS, ZRS (ZRS does not support Archive tier), GRS, GZRS, RA-GRS, RA-GZRS (RA-GZRS does not support Archive tier)
* Account Default Tier – Hot, Cool (Archive not available at the as a default account tier)

### Individual blob level settings 

* With replication option LRS/GRS/RA-GRS - All three access tiers hot, cool and archive can be set
* With replication option ZRS/GZRS/RA-GZRS - Only hot and cool access tiers can be set
 
Please change to a supported account type or replication option to use your preferred access tier. 

## **Recommended Documents**

* [Storage accounts that support tiering](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#storage-accounts-that-support-tiering)
* [Upgrade to a General-purpose v2 storage account](https://docs.microsoft.com/azure/storage/common/storage-account-upgrade)
* [Blob Storage Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#blob-storage-accounts)
* [General-purpose v2 Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts)

