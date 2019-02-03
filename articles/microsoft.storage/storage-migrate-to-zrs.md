<properties
	pageTitle="Convert to ZRS replication type"
	description="Self-help guide on how to convert to ZRS replication"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="raprasad"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32605567"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
	articleId="d7a99bd7-9456-4186-aae4-a4e6b85c0bf0"
/>

# Change to ZRS replication type

Changing redundancy type to zone-redundant storage (ZRS) involves moving the physical data from a single storage stamp to multiple stamps within a [qualified region](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#support-coverage-and-regional-availability). You have two primary options for converting to ZRS: manually copy or move data to a new ZRS account from your existing account, or request a live migration.

## **Recommended Steps**

Consider the following before to submitting a request for live migration to ZRS:

- Changing replication type from ZRS to LRS/GRS/RA-GRS is currently not supported. You will need to create a new storage account and manually migrate the data.
- Blob and GPv1 accounts will automatically be upgraded to GPv2 once the migration is complete. Make sure you review the [differences between the account types including billing](https://docs.microsoft.com/azure/storage/common/storage-account-overview).
- You must [manually convert your RA-GRS account(s) to GRS or LRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy#changing-replication-strategy) before requesting live migration to ZRS
- There are no ingress or egress costs associated with the live migration
- Empty LRS/GRS accounts won't be migrated. Please create a new ZRS account instead.
- You can only request a live migration within the same region - for example, an LRS account in East Asia cannot be converted to ZRS in US West 2 with live migration. You will need to perform the data migration manually.
- Live migration is only supported for Standard accounts. Premium accounts are not supported.
- You can only request a live migration in a [region where ZRS is supported](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#support-coverage-and-regional-availability)
- Changing replication type from ZRS Classic to ZRS is currently not supported. Our team is working on adding support for this operation. Once available you will be able to change the replication type to ZRS much like you upgrade from GPv1 to GPv2 account type.

## **Recommended Documents**

- [Converting to ZRS replication type](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#converting-to-zrs-replication)<br>
- [Azure Storage replication](https://docs.microsoft.com/azure/storage/common/storage-redundancy)<br>
- [Zone-redundant storage (ZRS): highly available Azure Storage applications](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs)
- [Data transfer for large datasets with low or no network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network)<br>
- [Data transfer for small datasets with low to moderate network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network)<br>
- [Data transfer for large datasets with moderate to high network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network)<br>
- [Solutions for periodic data transfer](https://docs.microsoft.com/azure/storage/common/storage-solution-periodic-data-transfer)<br>

