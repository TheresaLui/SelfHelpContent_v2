<properties
pageTitle="Access tiers is not supported on this storage account"
description="Access tiers is not supported on this storage account due to account type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_type_tiering_notSupported"
diagnosticScenario="Access tiers is not supported on this storage account"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Access tiers are not supported on this storage account

<!--issueDescription-->
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** does not support access tiers as it is a **<!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind-->** account. [Object storage data tiering to hot, cool, or archive is only supported in Blob storage and General Purpose v2 (GPv2) accounts](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#storage-accounts-that-support-tiering) and only available for block and append blobs. Please change to a supported account type to use access tiers.
<!--/issueDescription-->

## **Recommended Documents**

* [Storage accounts that support tiering](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#storage-accounts-that-support-tiering)
* [Blob Storage Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#blob-storage-accounts)
* [General-purpose v2 Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts)
