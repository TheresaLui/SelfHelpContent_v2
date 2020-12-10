<properties
      pageTitle="Check the customers storage account scenario"
      description="Check the customers storage account scenario"
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
      articleId="05ac8408-9cc1-4c05-8589-ad350d5ead9a"
      ownershipId="StorageMediaEdge_AccountManagement"
/>

# Check the customers storage account scenario

### Features of ZRS accounts.

1. Use Zone-redundant storage (ZRS) for building highly available Azure Storage applications
2. Zone-redundant storage (ZRS) replicates your data synchronously across three storage clusters in a single region.
   * Each storage cluster is physically separated from the others and is located in its own availability zone (AZ). 
   * Each availability zone. And the ZRS cluster within it. Is autonomous and includes separate utilities and networking features. 
   * A write request to a ZRS storage account returns successfully only after the data is written to all replicas across the three clusters.
3. A replication type change to ZRS will require (unlike other type changes which are just a type change in place and don't need any migration) a migration of data from old infrastructure to ZRS enabled infrastructure. 
   * This will be at whole account level and not endpoint level. To be handled by IaaS VM Storage POD.


