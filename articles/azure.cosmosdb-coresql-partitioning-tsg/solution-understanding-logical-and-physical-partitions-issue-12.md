<properties
	  pageTitle="Understanding Logical and Physical partitions issue"
	  description="Understanding Logical and Physical partitions issue"
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
	  articleId="f102cbce-d069-4b39-8fc2-334b45d3ac2e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Understanding Logical and Physical partitions issue

<!--issueDescription-->

Dear customer,

Please read below some facts about Logical and Physical partitions:

# Facts about logical partitions
- Each logical partition can hold up to 20GB of data.
- Logical partitions are placed on a particular physical partition. 
    * When documents are inserted, Azure Cosmos DB hashes the value of the partition key in the document, and assigns it to the physical partition whose assigned range includes the hashed value. 
- All data with the same logical partition key value will always be on the same physical partition. For example, if you partition by /UserId, and you have 100 documents where UserId = "Alice", all 100 will be on the same physical partition. 
- Multiple logical partitions can (and should be!) on the same physical partition
    * In fact, if a customer has picked a good partition key that has high cardinality, then each physical partition will contain many logical partitions. This is a good thing :)

# Facts about physical partitions
- Each physical partition can hold up to 50GB of data
- Each physical partition can support up to 10,000 RU/s
    * As a consequence, the theoretical RU/s a single logical partition can get is also 10,000 RU/s. 
- In Cassandra API only, the physical partition size is 30GB.
- As a historical note, prior to early 2018, we used to give 10GB physical partitions. In 2020, we migrated all external customers on 10GB physical partitions to 50GB. Since 2018, all new accounts have started with 50GB physical partitions (or 30GB for Cassandra)

For more details about partitions please refer to the following link:
- https://docs.microsoft.com/en-us/azure/cosmos-db/partitioning-overview

Thank you.

<!--/issueDescription-->

