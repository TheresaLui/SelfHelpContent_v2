<properties
	pageTitle="Azure Synapse Link for Cosmos DB - spark"
	description="Azure Synapse Link for Cosmos DB - spark"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32743029,32743057,32743058"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-spark"
	displayOrder="310"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB - Spark
Most users are able to resolve their Azure Synapse Link for Cosmos DB Spark issue using the steps below.  


## **Recommended Steps**  


### **Spark job failure** 
The most common challenge is memory pressure, because of improper configurations (particularly wrong-sized executors), long-running operations, and tasks that result in Cartesian operations. 

* [Use optimal data format](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-optimal-data-format) 
* [Use the cache](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-the-cache)
* [Use memory efficiently](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-memory-efficiently) 
* [Optimize data serialization](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-data-serialization)
* [Use bucketing](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-bucketing)
* [Optimize joins and shuffles](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-joins-and-shuffles) 
* [Optimize job execution](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-job-execution)

If the package the customer is installing is large or takes a long time to install, this affects the Spark instance startup time. [Please review Augmenting Apache Spark with additional libraries](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries)     

Spark pools in Azure Synapse include the following libraries that are available on the pools by default. 

* [Spark Core](https://spark.apache.org/docs/latest/) : Includes Spark Core, Spark SQL, GraphX, and MLlib. 
* [Anaconda](https://docs.continuum.io/anaconda/)  

**Solution**
[Monitor your Apache Spark applications](https://docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-spark-applications#accessing-the-list-of-spark-applications) 

<br>

### **Spark jobs latency**
You might experience some slowness in the Spark job that can be due to: 

* The Cosmos DB container that you want to access might not be located in the same region as your workspace. We recommend to deploy a workspace in the same data center as your Cosmos DB databases or simply replicate your container into the same region that you have your workspace in.  
* If your container and workspace are in the same region, make sure that you write a preferred region when you read or write with Spark. 

<br>

### *Select from Top 100 rows* gesture not working from a Spark Table pointing to a Cosmos DB container
*Failed to execute query. Error: Invalid object name* might be the error message that you get. Currently, Synapse metastore only syncs Spark and SQL Tables over parquet files in ADLsg2.  


**Solution**  
If you have access to SQL serverless support for Synapse Link, we recommend to create a view over the Azure Cosmos DB container that you want to access. 

<br>

## **Recommended Documents**  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support?toc=/azure/cosmos-db/toc.json&bc=/azure/cosmos-db/breadcrumb/toc.json)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.  


[Querying Azure Cosmos DB Analytical Store with Apache Spark for Azure Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark?toc=/azure/cosmos-db/toc.json&bc=/azure/cosmos-db/breadcrumb/toc.json)
<br>This article gives some examples on how you can interact with the analytical store from Synapse gestures.


