<properties
	  pageTitle="Issues related to Logical and Physical partitions"
	  description="Issues related to Logical and Physical partitions"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="17581f6f-b559-48e6-a555-7c0b24742ffd"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Issues related to Logical and Physical partitions

1. Before debugging an issue related "Why am I being throttled?", "How do I pick a good partition key?", or other issues in the Throughput/Scaling space, it's recommended to learn the fundamentals of logical and physical partitions.

2. Please read below more FAQs that customer's usually have and share with customer if it helps in anyway to inform or solve the issue:

### Is the Consumed Size include the Index size too?
Yes. The storage/ Partition consumption includes the index usage too.

### Does the source partition which is undergoing the split continue to take ingestion?
Yes it can take ingestion during the partition split.

### When does the source/old partition is degraded or decommissioned or not available for user activity?
The old partition is not available for user activity once the copy operation/switching is done.

### What happens to the application during the partition split
The application are allowed to continue to ingest and query the data against the old partition. The split task would swap the old partition to new partition at the last phase of the split process during that exact time (i.e. swap time) any request submitted to the old partition would be return 410s. The SDK handles the 410 by refreshing the partition key range to reflect the new partition information and retries the operation.

### What about scenarios where the # of physical partitions will decrease? 
Today, # of physical partitions can only ever increase. The ability to decrease or "merge" physical partitions is not available today. The team is working on enabling this capability. However, in the meantime, we recommend to customers they migrate their data to a new database/container to reset their physical partition layout if needed. 

### Can we have 50 GB logical partition size since we have increased the physical partition size?
No.

### Why does the partition size varies for different account? Why telemetry shows 10 GB physical partition, 20 GB and 50 GB?
Newly created Cosmos DB Account does create 50 GB Partitions. But the old Account continue to create 10 GB partition. There were custom configuration was done for certain Account to create 20 GB partition or 30 GB partition based on their user case and request.

The Cassandra accounts are by default are set to 30 GB Partition

### How long the partition split can take?
The actual partition split depends up on the rate of ingestion and the amount of data to be copied. The back ground task in its last phase of the split informs the old partition to not take any further request and initiates the swapping of old partition with the new partitions.The actual switching the new partition for old partition is done in less than 30 second in almost all cases except in some extreme situation it can go to up to 1 minute. The split task informs the old partition to accept any new request if for some reason the switch could not be completed in 1 minute and the application can continue to submit request to the old partition. Please note the swap would be retried again until the switch is completed successfully.

### What happens if a logical partition fills up to 20GB? Will Azure Cosmos DB split that?
No. Azure Cosmos DB will never split data in the same logical partition across multiple physical partitions, so if 20GB is filled up, no more writes will be accepted for data that would go into that logical partition. If this occurs, the customer should revisit their partitioning strategy. 

In practice, if you have 1KB documents to fill up 20GB for 1 logical partition, you would need 20,000,000 (20 million) documents for 1 key. We typically only see this in write-heavy IOT scenarios, where a single /vin, /deviceId/, /machineId actually does fill up 20GB. The guidance there is to choose a key with higher granularity (e.g. vin_date), or only keep recent data in Azure Cosmos DB with TTL. 

This also illustrates the importance of choosing a partition key with high cardinality. Suppose your partition key only had 2 values: True and False, and dataset you want to import is 100GB. You will certainly fill up 20GB across all data with partition key value = true and = false. To avoid this, you should choose a partition key with higher cardinality. 

### What is the terminology "offer replace?"
Within the Azure Cosmos DB team, changing the RU/s of a database or collection is often referred to internally as an "offer replace" operation. This is because in our resource model, there is an "Offers" object that describes the current RU/s settings, tied to a database or container. This is apparent if you use our [REST API](https://docs.microsoft.co/rest/api/cosmos-db/offers). 

However, in all other interfaces (SDK, Portal, PS, CLI) we abstract this offers resource, so users just see RU/s as a property they can change on their resource. As a result, users typically describe their operations as "changing RU/s", but when debugging internally, telemetry refers to "offer replace." 

### How do partition splits work behind the scenes?
When the split is triggered, a background tasks kicks in. The task creates 2 new physical partitions. It identifies the new partition width assigned to each and starts copying the data on the parent partition to the children, based on the partition key value. The actual time to do this copy step depends on the size of the data being copied. 

The application can continue to ingest data to the old partition until the copy and synchronization is complete. On average, the switch to start using the new physical partitions occurs in less than 30 seconds. In extreme cases, it can go up to a minute. 

### What's the impact to the customer's application during a split?
Applications can always ingest or query data during a split. Any request that happens to go to the old parent partition during the time period where the swap is ongoing (e.g. when the old parent partition isn't accepting operations anymore, but we haven't cutover to the new partitions yet) would get a 410 exception. The SDK handles this by refreshing its knowledge of the physical partition layout and retries the operation against the new partition. In theory, this retry operation can result in additional latency the 1st time the 410 is encountered, but in practice, the impact should be minimal. 

