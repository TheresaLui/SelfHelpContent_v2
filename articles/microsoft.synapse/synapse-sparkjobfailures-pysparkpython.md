<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "bigDataPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738793"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Spark Job Failures/PySpark (Python)"
	description = "Spark Job Failures/PySpark (Python)"
	articleId = "synapse-sparkjobfailures-pysparkpython"
	authors = "saltug"
	ms.author = "saltug"
/>

# Spark Job Failures/PySpark (Python)

## **Recommended Steps**

The most common challenge is memory pressure, because of improper configurations (particularly wrong-sized executors), long-running operations, and tasks that result in Cartesian operations. 
* [Use optimal data format](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-optimal-data-format)
* [Use the cache](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-the-cache)
* [Use memory efficiently](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-memory-efficiently)
* [Optimize data serialization](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-data-serialization)
* [Use bucketing](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-bucketing)
* [Optimize joins and shuffles](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-joins-and-shuffles)
* [Optimize job execution](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-job-execution)

If the package you are installing is large or takes a long time to install, this affects the Spark instance startup time. Please review [Augmenting Apache Spark with additional libraries](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries).

Spark pools in Azure Synapse include the following libraries that are available on the pools by default.
* [Spark Core](https://spark.apache.org/docs/latest/). Includes Spark Core, Spark SQL, GraphX, and MLlib.
* [Anaconda](https://docs.continuum.io/anaconda/)

## **Recommended Documents**

* [Monitor your Apache Spark applications](https://review.docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-spark-applications?branch=release-ignite-arcadia#accessing-the-list-of-spark-applications)