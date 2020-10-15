<properties
      pageTitle="ZRS Classic to ZRS Migration"
      description="ZRS Classic to ZRS Migration"
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
      articleId="46c415e2-c63b-44fd-9712-237607b241a5"
      ownershipId="StorageMediaEdge_AccountManagement"
/>

# ZRS Classic to ZRS Migration

### Migrating from a ZRS Classic to ZRS account.
1. Customers can self-initiate migrating from ZRS Classic to ZRS, in regions where ZRS is available, using Azure Portal.
   * > Note: ZRS requires custom infrastructure and is only available in regions that have [Availability Zones](https://docs.microsoft.com/en-us/azure/availability-zones/az-overview#regions-that-support-availability-zones)   
2. To upgrade to ZRS in the Azure portal, navigate to the **Configuration** section of the account and choose **Upgrade**:

###  Migration Directions from PowerShell
* To upgrade to ZRS using PowerShell call the following command:
	`Set-AzStorageAccount -ResourceGroupName  -AccountName  -UpgradeToStorageV2`

###  Migration Directions from CLI
* To upgrade to ZRS using CLI call the following command:
	`az storage account update -g  -n  --set kind=StorageV2`

### Recommended Documents
[Upgrade ZRS Classic to ZRS in the Portal](https://docs.microsoft.com/en-us/azure/storage/common/media/storage-redundancy-zrs/portal-zrs-classic-upgrade.png)
