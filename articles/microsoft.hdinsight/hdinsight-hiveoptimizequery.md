<properties
    pageTitle="My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636464"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0d3e4f2d-cfe6-4921-8395-750ac12be8c9"
	ownershipId="AzureData_HDInsight"
/>

# My Hive Queries Are Really Slow

## **Recommended Steps**

The following Hive performance optimization methods can be applied to your cluster:

 1. Scale out your worker nodes to leverage more mappers and reducers to be run in parallel
 2. Enable Tez as the execution engine instead of MapReduce
 3. Review your partitioning scheme to consider cases where there are too few or too many partitions. Choose the scheme such that the partitions are evenly sized.
 4. Use the ORCFile format which is optimized for faster access to data
 5. Enable vectorization to process multiple rows together

## **Recommended Documents**

* [Optimizing Hive Performance](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-optimize-hive-query)

### **Troubleshooting**

* [Why are my LLAP queries running slow?](https://hdinsight.github.io/hive/hive-llap-query-perf.html)
