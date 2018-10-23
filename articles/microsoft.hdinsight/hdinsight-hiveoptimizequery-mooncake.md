<properties
    pageTitle="My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32511190"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="MoonCake"
/>

# My hive queries are really slow

## **Recommended steps**
The following Hive performance optimization methods can be applied to your cluser:

 1. Scale out your worker nodes to leverage more mappers and reducers to be run in parallel.
 2. Enable Tez as the execution engine instead of MapReduce.
 3. Review your partitioning scheme to consider cases where there are too few or too many partitions. Choose the scheme such that the partitions are evenly sized.
 4. Use the ORCFile format which is optimized for faster access to data.
 5. Enable vectorization to process multiple rows together.

## **Recommended documents**
[Optimizing Hive Performance](https://docs.azure.cn/hdinsight/hdinsight-hadoop-optimize-hive-query)<br>
