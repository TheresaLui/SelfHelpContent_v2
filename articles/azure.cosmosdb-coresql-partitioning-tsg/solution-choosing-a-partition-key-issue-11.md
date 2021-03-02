<properties
	  pageTitle="Choosing a partition key issue"
	  description="Choosing a partition key issue"
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
	  articleId="c617c682-9581-4195-b6a5-1faa50646f81"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Choosing a partition key issue

<!--issueDescription-->

Dear customer,

The following is a good guidance for choosing a partition key:  
* A single logical partition has an upper limit of 20 GB of storage. This cannot be increased any further.  
* Azure Cosmos containers have a minimum throughput of 400 request units per second (RU/s). When throughput is provisioned on a database, minimum RUs per container is 100 request units per second (RU/s). Requests to the same partition key can't exceed the throughput that's allocated to a partition. If requests exceed the allocated throughput, requests are rate-limited. So, it's important to pick a partition key that doesn't result in "hot spots" within your application.  
* Choose a partition key that has a wide range of values and access patterns that are evenly spread across logical partitions. This helps spread the data and the activity in your container across the set of logical partitions, so that resources for data storage and throughput can be distributed across the logical partitions.  
* Choose a partition key that spreads the workload evenly across all partitions and evenly over time. Your choice of partition key should balance the need for efficient partition queries and transactions against the goal of distributing items across multiple partitions to achieve scalability.  
* Candidates for partition keys might include properties that appear frequently as a filter in your queries. Queries can be efficiently routed by including the partition key in the filter predicate.

Please use the below document for more details on how to chooses a Partition Key:
- https://docs.microsoft.com/en-us/azure/cosmos-db/partitioning-overview#choose-partitionkey

Thank you.

<!--/issueDescription-->

