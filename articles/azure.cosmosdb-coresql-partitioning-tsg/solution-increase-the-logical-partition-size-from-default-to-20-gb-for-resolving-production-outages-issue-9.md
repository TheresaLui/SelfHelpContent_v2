<properties
	  pageTitle="Increase the Logical Partition Size from default to 20 GB for resolving Production outages issue"
	  description="Increase the Logical Partition Size from default to 20 GB for resolving Production outages issue"
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
	  articleId="61d3d801-37a5-4a08-8f40-0ce83dbfbaa3"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Increase the Logical Partition Size from default to 20 GB for resolving Production outages issue

<!--issueDescription-->

Dear customer

In the document [Azure Cosmos DB service quotas](https://docs.microsoft.com/en-us/azure/cosmos-db/concepts-limits#provisioned-throughput), the limit of logical partition maximum size is **20 GB** now. 

#### Partition key(Logical partition) reached maximum size of 20 GB. Is it possible to increase the logical partition size? 
The logical partition size is a limit which has been there from start of the product and documented [here](https://docs.microsoft.com/en-us/azure/cosmos-db/partitioning-overview#logical-partitions) - 'There is no limit to the number of logical partitions in your container. Each logical partition <u>can store up to 20 GB of data.</u>'
<br>No, it is not possible to increase the logical partition size if it hits 20 GB.

#### Logical Partition Size Limit can be hit for all collections.
The logical size limit can be hit for both Fixed collection and partitioned collection.  

#### Error message when hitting the Logical Partition Size Limit.
"Error: Partition key reached maximum size of 20 gb."

#### How to resolve the issue when customer hits the Logical Partition Size Limit?
- If a you are hitting the 20 GB limit, you have to change the partition key and migrate the data.

- Before migrating data to a new collection, you need to know how to [choose a good partition key](https://docs.microsoft.com/en-us/azure/cosmos-db/partitioning-overview#choose-partitionkey), so each logical partition has a wide range of possible values. 
<br>For example, in a container where all items contain a foodGroup property, the data within the Beef Products logical partition can grow up to 20 GB. Selecting a partition key with a wide range of possible values ensures that the container is able to scale, so it will not hit the logical partition limit again.

- The customer can refer to the doc [Migrate non-partitioned containers to partitioned containers](https://docs.microsoft.com/en-us/azure/cosmos-db/migrate-containers-partitioned-to-nonpartitioned) if the collection is a fixed collection. This option does require application change.

- Options to migrate the data - [Options to migrate your on-premises or cloud data to Azure Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/cosmosdb-migrationchoices)

Thank you.

<!--/issueDescription-->

