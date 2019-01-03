<properties
    pageTitle="My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    authoralias="bharathb"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds="32629065"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="MoonCake"
/>

# My hive queries are really slow

## **Recommended Steps**

The following Hive performance optimization methods can be applied to your cluster:

1. Scale out your worker nodes to leverage more mappers and reducers to be run in parallel
2. Enable Tez as the execution engine instead of MapReduce
3. Review your partitioning scheme to consider cases where there are too few or too many partitions, and choose the scheme where the partitions are evenly sized
4. Use the ORCFile format, which is optimized for faster access to data
5. Enable vectorization to process multiple rows together

## **Recommended Documents**

* [Optimizing Hive Performance](https://docs.azure.cn/hdinsight/hdinsight-hadoop-optimize-hive-query)<br>
