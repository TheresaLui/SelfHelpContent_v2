<properties
    pageTitle="Azure HDInsights: My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="bharathb, jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636458"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public,MoonCake"
    articleId="913102d6-193a-48b4-b259-64fd4927379e"
/>

# Hive Performance

## **Recommended Steps**

The following Hive performance optimization methods can be applied to your cluster:

 1. Scale out your worker nodes to leverage more mappers and reducers to be run in parallel
 2. Enable Tez as the execution engine instead of MapReduce
 3. Review your partitioning scheme to consider cases where there are too few or too many partitions. Choose the scheme such that the partitions are evenly sized.
 4. Use the ORCFile format which is optimized for faster access to data
 5. Enable vectorization to process multiple rows together

## **Recommended Documents**

* [Optimize Apache Hive queries in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-optimize-hive-query)
