<properties
      pageTitle="Migrating RA-GRS to ZRS"
      description="Migrating RA-GRS to ZRS"
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
      articleId="154f4132-4aab-47b2-baa7-273320991c8d"
      ownershipId="StorageMediaEdge_AccountManagement"
/>

# Migrating RA-GRS to ZRS

### Migrating RA-GRS to ZRS not supported

1. User wants to migrate from RA-GRS to ZRS.
2. This scenario is not supported.
3. Please update customer with the following message. 
> Migrating from RA-GRS is not supported. You must first convert to either LRS or GRS before submitting live migration request. Use the Azure portal or the Storage Resource Provider API to change your account's redundancy type. Azure will then replicate your data accordingly.
> 
Check [here](https://docs.microsoft.com/en-us/azure/storage/common/redundancy-migration?tabs=portal) for more details.
