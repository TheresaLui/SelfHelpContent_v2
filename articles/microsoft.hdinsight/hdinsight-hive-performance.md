<properties
    pageTitle="My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="bharathb"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629065"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="MoonCake, Fairfax"
	articleId="a53099e6-974e-4cfe-8a0c-92949362cbd8"
	ownershipId="AzureData_HDInsight"
/>

# Hive Queries are Slow

## **Recommended Steps**

The following Hive performance optimization methods can be applied to your cluster:

1. [Scale out](https://docs.azure.cn/zh-cn/hdinsight/hdinsight-hadoop-optimize-hive-query#scale-out-worker-nodes) your worker nodes to leverage more mappers and reducers to be run in parallel
2. [Enable Tez](https://docs.azure.cn/zh-cn/hdinsight/hdinsight-hadoop-optimize-hive-query#enable-tez) as the execution engine instead of MapReduce
3. Review your [partitioning scheme](https://docs.azure.cn/zh-cn/hdinsight/hdinsight-hadoop-optimize-hive-query#hive-partitioning) to consider cases where there are too few or too many partitions, and choose the scheme where the partitions are evenly sized
4. Use the [ORCFile format](https://docs.azure.cn/zh-cn/hdinsight/hdinsight-hadoop-optimize-hive-query#use-the-orcfile-format), which is optimized for faster access to data
5. Enable [vectorization](https://docs.azure.cn/zh-cn/hdinsight/hdinsight-hadoop-optimize-hive-query#vectorization) to process multiple rows together

## **Recommended Documents**

* [Optimizing Hive Performance](https://docs.azure.cn/hdinsight/hdinsight-hadoop-optimize-hive-query)<br>
