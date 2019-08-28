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
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** does not support access tiers as it is a **<!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind-->** account. Access tiers are only available for block and append blobs, and are only supported on Blob Storage Accounts, General-purpose v2 Accounts, and Premium Block Blob Storage Accounts (in limited preview). Please upgrade to a supported account type to use access tiers.
<!--/issueDescription-->

## **Recommended Documents**

* [Access tiers](https://docs.microsoft.com/azure/storage/common/storage-account-overview#access-tiers-for-block-blob-data)
* [Premium Block Blob Storage Account](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#premium-access-tier)
* [Blob Storage Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#blob-storage-accounts)
* [General-purpose v2 Accounts](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts)
