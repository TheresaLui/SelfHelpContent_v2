<properties
	pageTitle="Convert to GZRS replication type"
	description="Self-help guide on how to convert to GZRS replication."
	service="microsoft.storage"
	resource="storageaccounts"
	authors="ramMSFT"
	ms.author="raprasad"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32634987"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	articleId="97cfa678-48dd-4769-9473-43100aa5b481"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Change to GZRS replication type

Converting from LRS/ GRS/ RA-GRS/ ZRS to (RA-)GZRS is supported. To convert from ZRS to (RA-)GZRS you can use Azure CLI, Azure PowerShell, Azure Portal, Azure Resource Manager, and the Azure Storage Management SDK.

Changing redundancy type to geo and zone redundant storage (GZRS) from non-ZRS accounts involves moving the data from a single storage stamp to multiple stamps within a [qualified region](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#support-coverage-and-regional-availability). You have two primary options for converting to (RA-)GZRS: manually copy or move data to a new (RA-)GZRS account from your existing account, or request a live migration.

## **Recommended Steps**

Consider the following before to submitting a request for live migration to (RA-)GZRS:

- Changing replication type from (RA-)GZRS to LRS/GRS/RA-GRS is currently not supported. You will need to create a new storage account and manually migrate the data back.
- Blob and GPv1 accounts will automatically be upgraded to GPv2 once the migration is complete. Make sure you review the [differences between the account types including billing](https://docs.microsoft.com/azure/storage/common/storage-account-overview).
- There are no ingress or egress costs associated with the live migration
- Empty LRS/GRS accounts won't be migrated. Please create a new (RA-)GZRS account instead.
- You can only request a live migration within the same region - for example, an LRS account in East Asia cannot be converted to (RA-)GZRS in US West 2 with live migration. You will need to perform the data migration manually.
- Live migration is only supported for Standard accounts. Premium accounts are not supported.
- You can only request a live migration in a [region where ZRS is supported](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#support-coverage-and-regional-availability)
- While Microsoft handles your request for live migration promptly, there's no guarantee as to when a live migration will complete. If you need your data migrated to (RA-)GZRS by a certain date, then Microsoft recommends that you perform a manual migration instead. Generally, the more data you have in your account, the longer it takes to migrate that data.
- Managed disks are only available for LRS and cannot be migrated to (RA-)GZRS. You can store snapshots and images for Standard SSD Managed Disks on Standard HDD storage and choose between LRS and ZRS options.

## **Recommended Documents**

- [Converting to ZRS replication type](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#converting-to-zrs-replication)<br>
- [Azure Storage replication](https://docs.microsoft.com/azure/storage/common/storage-redundancy)<br>
- [Zone-redundant storage (ZRS): highly available Azure Storage applications](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs)
- [Data transfer for large datasets with low or no network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network)<br>
- [Data transfer for small datasets with low to moderate network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network)<br>
- [Data transfer for large datasets with moderate to high network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network)<br>
- [Solutions for periodic data transfer](https://docs.microsoft.com/azure/storage/common/storage-solution-periodic-data-transfer)<br>