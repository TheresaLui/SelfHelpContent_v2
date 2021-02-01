<properties
      pageTitle="Migrating a Premium Storage Account"
      description="Migrating a Premium Storage Account"
      service="Microsoft.Storage"
      resource="Microsoft.Storage/storageAccounts"
      authors="yoginm"
      ms.author="yomashru"
      displayOrder=""
      selfHelpType="TSG_Content"
      supportTopicIds=""
      resourceTags=""
      productPesIds=""
      cloudEnvironments="public, fairfax, usnat, ussec"
      articleId="e8b3080a-4c26-4078-bf60-8a106ad203c4"
      ownershipId="StorageMediaEdge_AccountManagement"
/>

# Migrating a Premium Storage Account

###  Migrating a premium storage account to ZRS is not supported.

1. User wants to migrate a premium storage account.
2. This scenario is not supported.
3. CSS engineer validates that the storage account is Premium storage account.
   * It can be checked in ASC > In storage accoutn properties. 
4. If Premium storage account, then update customer with the following message.
      > We currently do not support migrating from a premium storage account to ZRS. Only standard account migration is supported.

### Recommended Documents
Some of the ways we can manually transfer are documented [here](https://docs.microsoft.com/en-us/azure/storage/common/storage-choose-data-transfer-solution)
