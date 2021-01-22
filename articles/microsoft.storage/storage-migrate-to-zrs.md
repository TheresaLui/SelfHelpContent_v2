<properties
	pageTitle="Convert to ZRS replication type"
	description="Self-help guide on how to convert to ZRS replication"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="lea"
	ms.author="leakkari"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32605567,32691090"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	articleId="d7a99bd7-9456-4186-aae4-a4e6b85c0bf0"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Change to ZRS replication type

Changing redundancy type to zone-redundant storage (ZRS) involves moving the physical data from a single storage stamp to multiple stamps within a [qualified region](https://docs.microsoft.com/azure/storage/common/storage-redundancy#zone-redundant-storage). 

## **Recommended Steps**

You have [two migration options](https://docs.microsoft.com/azure/storage/common/redundancy-migration?tabs=portal#perform-a-manual-migration-to-zrs-gzrs-or-ra-gzrs) for converting to ZRS:

- Manual Migration: Manually copy or move data to a new ZRS account from an existing account. If you need the migration to complete by a certain date consider performing a manual migration.
- Live Migration: If your application requires high availability, Microsoft also provides a live migration option. A live migration is an in-place migration with no downtime. 

Before to submitting a request for live migration to ZRS, consider the following:
   - There are no ingress or egress costs associated with the live migration
   - You must [manually convert your RA-GRS accounts to GRS or LRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy#changing-replication-strategy) before requesting live migration to ZRS
   - You can only request a live migration in a [region where ZRS is supported](https://docs.microsoft.com/azure/storage/common/storage-redundancy#zone-redundant-storage)
   - Costs associated to your account may vary.  For costs asssociated with different redundancy options [see pricing details](https://azure.microsoft.com/pricing/details/storage/blobs/?OCID=AID2100131_SEM_44cd34dfe0551f34d5ac54d8cbed6754%3AG%3As&ef_id=44cd34dfe0551f34d5ac54d8cbed6754%3AG%3As&msclkid=44cd34dfe0551f34d5ac54d8cbed6754). Additionally, Blob and GPv1 accounts will automatically be upgraded to GPv2 once the migration is complete. Make sure to review the [differences between the account types including billing](https://docs.microsoft.com/azure/storage/common/storage-account-overview).


## **Recommended Documents**

- [Converting to ZRS replication type](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#converting-to-zrs-replication)<br>
- [Pricing for different redundancy options](https://azure.microsoft.com/pricing/details/storage/blobs/?OCID=AID2100131_SEM_44cd34dfe0551f34d5ac54d8cbed6754:G:s&ef_id=44cd34dfe0551f34d5ac54d8cbed6754:G:s&msclkid=44cd34dfe0551f34d5ac54d8cbed6754)
- [Azure Storage replication](https://docs.microsoft.com/azure/storage/common/storage-redundancy)<br>
- [Data transfer for large datasets with low or no network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network)<br>
- [Data transfer for small datasets with low to moderate network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network)<br>
- [Data transfer for large datasets with moderate to high network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network)<br>
- [Solutions for periodic data transfer](https://docs.microsoft.com/azure/storage/common/storage-solution-periodic-data-transfer)<br>

