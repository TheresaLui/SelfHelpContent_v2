<properties
	  pageTitle="Understand what circumstances can the number of physical partitions change"
	  description="Understand what circumstances can the number of physical partitions change"
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
	  articleId="c206f24a-6b36-4e6b-aeb7-538822b77c47"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Understand what circumstances can the number of physical partitions change

<!--issueDescription-->

Dear customer,

After a user has created their resource (database or container), the number of physical partitions can only change (i.e. increase) if one of the two scenarios happens: 

## Scenario 1: User increases their RU/s beyond what their current partitioning layout can support.
This is an user-initiated action. Changing the RU/s can be done through the Azure portal, or programatically with REST API, SDK, PowerShell, or CLI.

When the user initiates the scale-up, Azure Cosmos DB will split existing physical partitions until the customer has the minimum number of physical partitions needed to support the desired RU/s. 

How do we know the minimum number of physical partitions needed? By the fact each physical partition can support up to 10,000 RU/s. 

> **Formula**: New # of physical partitions = current # of physical partitions + ROUNDUP([new RU/s - (current # of physical partitions * 10,000 RU/s)] / 10,000). 

In the following examples, note how depending on the current physical partition layout and the desired RU/s, some scale-up operations are instant, and some are asynchronous (can take up to 5-6 hours).

#### Example 1
- Alice creates a manual collection with dedicated throughput of 20,000 RU/s. This creates 4 physical partitions. Each physical partition has 20,000 RU/s / 4 = 5000 RU/s. 
- Alice now scales to 25,000 RU/s. 
    * Does Azure Cosmos DB trigger a split? 
        * No. With 4 physical partitions, and each partition being able to support 10,000 RU/s, the user could scale up to 40,000 RU/s without triggering a split. 
        * Because 25,000 RU/s is achievable with the existing 4 physical partitions, no split is needed. 
        * As a result, the scale-up operation is instantaneous. 
        * Each physical partition now has 25,000 / 4 = 6250 RU/s. 



- Alice now decides to scale to 75,000 RU/s
    * Does Azure Cosmos DB trigger a split? 
        * Yes. Intuitively, to handle 75,000 RU/s, Azure Cosmos DB would need at least 8 physical partitions. We always split until we reach the minimum # of physical partitions needed, so the user will end with 8 physical partitions at the end. 
        * As a result, the scale-up operation is asynchronous, and can take up to 5-6 hours. 
        * New # of physical partitions = 4 + ROUNDUP([(75,000 - (4 * 10,000)) / 10,000]) = 8. 

#### Example 2
- Alice creates an autoscale shared throughput database with max RU/s = 35,000 RU/s (scales between 3500- 35,000 RU/s) This creates 4 physical partitions.
- Alice now changes the autoscale max RU/s to 40,000 RU/s (scales between 4000 - 40,000 RU/s). 
    * Does Azure Cosmos DB trigger a split? 
        * With 4 physical partitions, and each partition being able to support 10,000 RU/s, the user increase the max RU/s to 40,000 RU/s without triggering a split. As a result, the scale-up operation is instantaneous. 
        * Because 40,000 RU/s is achievable with the existing 4 physical partitions, no split is needed. 
- Alice now decides to scale their autoscale max RU/s to 50,000 RU/s
    * Does Azure Cosmos DB trigger a split? 
        * Yes. Intuitively, to handle 50,000 RU/s, Azure Cosmos DB would need at least 5 physical partitions. We always split until we reach the minimum # of physical partitions needed, so the user will end with 5 physical partitions at the end. 
        * As a result, the scale-up operation is asynchronous, and can take up to 5-6 hours. 
        * New # of physical partitions = 4 + ROUNDUP([(50,000 - (4 * 10,000)) / 10,000]) = 5.  

## Scenario 2: Azure Cosmos DB system automatically splits a physical partition due to storage
When a physical partition reaches 97% of its 50GB capacity, Azure Cosmos DB will automatically split that physical partition into 2 physical partitions. The user contributes indirectly to this split, as they have inserted data into the system, but do not directly trigger the split themselves. 

This is a value prop of the system, as the user does not have to worry about managing physical partitions if they fill up the storage. 

Thank you.

<!--/issueDescription-->

