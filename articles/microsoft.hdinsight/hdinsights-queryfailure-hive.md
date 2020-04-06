<properties
    pageTitle="Azure HDInsights Query or Job Failure: Hive"
    description="Azure HDInsight Hive Troubleshooting"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636459"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax"
    articleId="4099d7f3-cc14-4320-8844-dc389d25ba96"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight Hive Troubleshooting

## **Recommended Steps**

### **Troubleshooting**

* Job failures/long running jobs could be caused due to insufficient resources on the cluster for yarn to allocate containers for already executing applications. We recommend to retry the job when sufficient resources are available. You can check Ambari for 
available resources by following article [here](https://docs.microsoft.com/azure/hdinsight/hdinsight-changing-configs-via-ambari#apache-hive-optimization).
* Check out [Apache Hive Optimization](https://docs.microsoft.com/azure/hdinsight/hdinsight-changing-configs-via-ambari#apache-hive-optimization) for configuration options like vectorization, parallel execution, and more which will optimize your Apache Hive performance
* [How to resolve poor performance in Apache Hive LLAP queries in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/interactive-query/interactive-query-troubleshoot-query-performance)
* [Troubleshoot Apache Hive by using Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-hive)
* [How to resolve Out of Memory error?](https://hdinsight.github.io/hive/hive-join-oom.html)

**Error: Hive is down on the LLAP server.**

Cause: the OS was not able to give any more threads to Hive Metastore service

Solution: Hive metastore service should run with fewer threads than the default.  Suggest setting the value of hive.metastore.server.max.threads to 50000. [For more information read here](https://cwiki.apache.org/confluence/display/Hive/AdminManual%2BMetastore%2BAdministration)

### **Configuration**

* [Scheduling Hive queries](https://docs.microsoft.com/azure/hdinsight/hadoop/hdinsight-use-hive#scheduling-hive-queries)
* [Use Apache Hive to query Apache Hbase](https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-tutorial-get-started-linux#use-apache-hive-to-query-apache-hbase)
* [Configure Apache Hive ranger policies to restrict access to Hive tables](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-run-hive)
* [Run Apache Hive queries using the Data Lake tools for Visual Studio](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-hadoop-use-hive-visual-studio)

## **Recommended Documents**

* [Refresh the HDInsight certificate for Data Lake Storage Gen1 access](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store?toc=/azure/hdinsight/hadoop/TOC.json&bc=/azure/bread/toc.json#refresh-the-hdinsight-certificate-for-data-lake-storage-gen1-access)

