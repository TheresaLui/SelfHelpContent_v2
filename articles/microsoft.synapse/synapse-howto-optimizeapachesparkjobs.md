<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "bigDataPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738784"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "How-To/Optimize Apache Spark jobs"
	description = "How-To/Optimize Apache Spark jobs"
	articleId = "synapse-howto-optimizeapachesparkjobs"
	authors = "saltug"
	ms.author = "saltug"
/>

# How-To/Optimize Apache Spark jobs

## **Recommended Steps**

If the package you are installing is large or takes a long time to install, this affects the Spark instance start up time. Please review review [Augmenting Apache Spark with additional libraries](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries).

The most common challenge is memory pressure, because of improper configurations (particularly wrong-sized executors), long-running operations, and tasks that result in Cartesian operations. 
* [Use optimal data format](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-optimal-data-format)
* [Use the cache](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-the-cache)
* [Use memory efficiently](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-memory-efficiently)
* [Optimize data serialization](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-data-serialization)
* [Use bucketing](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#use-bucketing)
* [Optimize joins and shuffles](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-joins-and-shuffles)
* [Optimize job execution](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance?branch=release-ignite-arcadia#optimize-job-execution)

## **Recommended Documents**

* [Create Apache Spark job definition](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-job-definitions?branch=release-ignite-arcadia)
* [Spark instances](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-concepts?branch=release-ignite-arcadia#spark-instances)
* [Delta Lake](https://review.docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-what-is-delta-lake?branch=release-ignite-arcadia)