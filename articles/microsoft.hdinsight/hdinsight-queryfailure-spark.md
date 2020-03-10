<properties
    pageTitle="Azure HDInsights Query Failure - Spark "
    description="Azure HDInsights Query Failure - Spark "
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636496"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax"
    articleId="302b8254-83e6-4005-9d2e-891f19ebc0f3"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsights Query Failure - Spark

## **Recommended Steps**

### **Configuration**

* [Troubleshoot Apache Spark by using Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark#how-do-i-configure-an-apache-spark-application-by-using-spark-submit-on-clusters)
* [Use Apache Spark REST API to submit remote jobs to an HDInsight Spark cluster](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-livy-rest-interface)
* [Using Spark-Submit to create Apache Spark jobs](https://hdinsight.github.io/spark/spark-submit-chronicles.html)

### **Troubleshooting**

* [Debug Apache Spark jobs running on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-job-debugging)
* [Streaming Application Fails Without Error](https://hdinsight.github.io/spark/spark-stream-session-configuration.html)
* [Use extended Apache Spark History Server to debug and diagnose Apache Spark applications](https://docs.microsoft.com/azure/hdinsight/spark/apache-azure-spark-history-server)
* [Debug Apache Spark applications locally or remotely on an HDInsight cluster with Azure Toolkit for IntelliJ through SSH](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-intellij-tool-debug-remotely-through-ssh)
* [Apache Spark jobs run slowly when the Azure storage container contains many files](https://hdinsight.github.io/spark/spark-job-slowness-when-destination-folder-has-too-many-files)
* [Known timeout issue with Anaconda version 4.7.11 and 4.7.12](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-python-package-installation#known-issue)

### **Solutions to common errors encountered**

* [IllegalArgumentException](https://hdinsight.github.io/spark/spark-application-fails-IllegalArgumentException.html)
* [LISTSTATUS failed with error 0x83090aa2 (Forbidden. ACL verification failed. Either the resource does not exist or the user is not authorized to perform the requested operation.)](https://hdinsight.github.io/ClusterManagement/hdinsight-adlsaccessissues.html)
* [InvalidClassException](https://hdinsight.github.io/spark/spark-class-version-mismatch-InvalidClassException.html)
* [NativeAzureFileSystem ... RequestBodyTooLarge](https://hdinsight.github.io/spark/spark-stream-driver-logs-error-requestbodytoolarge.html)
* [Spark Application Fails with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)
* Spark Application Fails with OutOfMemoryError on one node only: This could be due to skew. A frequent solution to skew is to use broadcast plans by changing the broadcast threshold value. The threshold can be configured using `spark.sql.autoBroadcastJoinThreshold`

### **Steps to check for resource allocation issues:**


* Make sure that the cluster to be used has enough resources by verifying the applications currently running in spark cluster, using Yarn UI. Another source of information about the resources being used by the Spark Executors is the Spark Application UI. In the Spark UI, select the Executors tab to display Summary and Detail views of the configuration and resources consumed by the executors. These views can help you determine whether to change default values for Spark executors for the entire cluster, or a particular set of job executions.
* Depending on your Spark workload, you may determine that a non-default Spark configuration provides more optimized Spark job executions. You should perform benchmark testing with sample workloads to validate any non-default cluster configurations. Some of the common parameters that you may consider adjusting are:

    * --num-executors sets the number of executors
    * --executor-cores sets the number of cores for each executor
    * --executor-memory controls the memory size (heap size) of each executor on Apache Hadoop YARN, and you'll need to leave some memory for execution overhead
    
* Following command is an example of how to change the configuration parameters for a batch application that is submitted using spark-submit: `spark-submit --class --executor-memory 3072M --executor-cores 4 –-num-executors 10`

## **Recommended Documents**

* [Access YARN application logs on Linux-based HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)
* [How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)
* [Spark Application Failed with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)
* [Refresh the HDInsight certificate for Data Lake Storage Gen1 access](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store?toc=/azure/hdinsight/hadoop/TOC.json&bc=/azure/bread/toc.json#refresh-the-hdinsight-certificate-for-data-lake-storage-gen1-access)
