<properties
      pageTitle="Source LRS account with data"
      description="Source LRS account with data"
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
      articleId="4ef3744d-d3a2-41e0-b847-713726dded78"
      ownershipId="StorageMediaEdge_AccountManagement"
/>

# Source LRS account with data

##  Migrating LRS account with data to ZRS.
1. User wants to migrate non empty LRS to ZRS.
   * Account is LRS and has data.
   * This is supported.
2. CSS files ICM ticket and places it in the appropriate queue/path: **Azure/XStore/Capacity Management**
   * Use this [ICM Template](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=34b2b2).
