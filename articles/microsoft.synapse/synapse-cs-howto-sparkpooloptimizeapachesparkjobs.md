<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "bigDataPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783919"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "How-To/Spark pool - Optimize Apache Spark jobs"
    description = "How-To/Spark pool - Optimize Apache Spark jobs"
    articleId = "synapse-cs-howto-sparkpooloptimizeapachesparkjobs.md"
    ms.author = "saltug"
/>

# How-To/Spark pool - Optimize Apache Spark jobs

## **Recommended Steps**

If the package you are installing is large or takes a long time to install, this affects the Spark instance startup time. Please review [Augmenting Apache Spark with additional libraries](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-azure-portal-add-libraries).

The most common challenge is memory pressure, because of improper configurations (particularly wrong-sized executors), long-running operations, and tasks that result in Cartesian operations. 

* [Use optimal data format](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-optimal-data-format)

* [Use the cache](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-the-cache)

* [Use memory efficiently](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-memory-efficiently)

* [Optimize data serialization](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-data-serialization)

* [Use bucketing](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#use-bucketing)

* [Optimize joins and shuffles](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-joins-and-shuffles)

* [Optimize job execution](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-performance#optimize-job-execution)

## **Recommended Documents**

* [Create Apache Spark job definition](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-job-definitions)

* [Spark instances](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-concepts#spark-instances)

* [Delta Lake](https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-what-is-delta-lake)

 