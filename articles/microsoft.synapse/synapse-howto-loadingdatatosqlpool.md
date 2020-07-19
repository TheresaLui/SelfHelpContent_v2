<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738778"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/Loading Data to SQL pool"
	description = "How-To/Loading Data to SQL pool"
	articleId = "synapse-howto-loadingdatatosqlpool"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/Loading Data to SQL pool

## **Recommended Steps**

Always leverage Polybase to batch load into your SQL pool and avoid singleton inserts.

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance
* Make sure to co-locate your staging area (blob storage or data lake store) and your SQL pool to minimize latency
* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL p[ool] increases the numbers of readers and writers for parallelism.

## **Recommended Documents**

* [Best practices when loading into SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)<br>
* [Designing a Polybase data loading strategy for SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

