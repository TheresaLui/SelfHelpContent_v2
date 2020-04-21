<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "bigDataPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738803"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Spark Job Execution Performance/Spark (Scala)"
	description = "Spark Job Execution Performance/Spark (Scala)"
	articleId = "synapse-sparkjobexecutionperformance-sparkscala"
	authors = "saltug"
	ms.author = "saltug"
/>

# Spark Job Execution Performance/Spark (Scala)

## **Recommended Steps**

The most common challenge is memory pressure, because of improper configurations (particularly wrong-sized executors), long-running operations, and tasks that result in Cartesian operations. 
* [Use optimal data format](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-optimal-data-format)
* [Use the cache](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-the-cache)
* [Use memory efficiently](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-memory-efficiently)
* [Optimize data serialization](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-data-serialization)
* [Use bucketing](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-bucketing)
* [Optimize joins and shuffles](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-joins-and-shuffles)
* [Optimize job execution](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-job-execution)

If the package you are installing is large or takes a long time to install, this affects the Spark instance startup time. Please review [Augmenting Apache Spark with additional libraries](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries).

Spark pools in Azure Synapse include the following libraries that are available on the pools by default.
* [Spark Core](https://spark.apache.org/docs/latest/). Includes Spark Core, Spark SQL, GraphX, and MLlib.
* [Anaconda](https://docs.continuum.io/anaconda/)

## **Recommended Documents**

* [Monitor your Apache Spark applications](https://docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-spark-applications#accessing-the-list-of-spark-applications)
