<properties
	  pageTitle="Know how many physical partitions does a database or collection start with"
	  description="Know how many physical partitions does a database or collection start with"
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
	  articleId="95a235a8-1ca7-4555-8a7f-959b3b66f5ef"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Know how many physical partitions does a database or collection start with

<!--issueDescription-->

Dear customer,

When a user first creates a database or container, the only information we have about the workload is the starting number of RU/s the customer wants to provision. Azure Cosmos DB uses a heuristic to determine how many physical partitions a database or container should start with. 

Note that for collections with dedicated manual throughput, the denominator is 6000, not 10,000. 

|**Throughput type**  |**Resource type**  | **Number of physical partitions** | **Example**|
|--|--|--|--|
|Manual  | Collection with dedicated throughput | # physical partitions = ROUNDUP(starting RU/s / 6000) | Example: You start with 400 RU/s. This creates 1 physical partition. <br><br> Example: You start with 10,000 RU/s. This creates 2 physical partitions.  |
|Manual | Database with shared throughput |# physical partitions = ROUNDUP(starting RU/s / 10,000)  | Example: You start with 35,000 RU/s. This creates 4 physical partitions. <br><br> Example: You start with 10,000 RU/s. This creates 1 physical partition.  |
|Autoscale | Collection with dedicated throughput  |# physical partitions = ROUNDUP(starting RU/s / 10,000)  | Example: You start with autoscale max RU/s of 25,000 RU/s (scales between 2500 - 25,000 RU/s. This creates 3 physical partitions. <br><br> Example: You start with autoscale max RU/s of 4000 RU/s (scales between 400 - 4000 RU/s). This creates 1 physical partition.  |
|Autoscale | Database with shared throughput  |# physical partitions = ROUNDUP(starting RU/s / 10,000)  | See above |


Thank you.

<!--/issueDescription-->

