<properties
    pageTitle="Spark application configuration"
    description="Spark application configuration"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="v-anukar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636495"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
    articleId="1cc6f5a8-476c-4638-9a5b-be97b0640439"
	ownershipId="AzureData_HDInsight"
/>

# Spark Application Configuration

## **Recommended Documents**


* The amount of memory and number of cores that a Spark application can use can be configured through [Ambari](https://hdinsight.github.io/spark/spark-application-configuration-through-ambari.html), [spark-submit](https://hdinsight.github.io/spark/spark-application-configuration-through-spark-submit.html), [LIVY](https://hdinsight.github.io/spark/spark-application-configuration-through-livy.html), or [Jupyter notebooks](https://hdinsight.github.io/spark/spark-application-configuration-through-jupyter.html)
* [Troubleshoot a slow or failing job on a HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster)
* [Debug Apache Spark jobs running on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-job-debugging)
* [Use extended Apache Spark History Server to debug and diagnose Apache Spark applications](https://docs.microsoft.com/azure/hdinsight/spark/apache-azure-spark-history-server)
* [Scenario: Apache Spark job run slowly when the Azure storage container contains many files in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-troubleshoot-job-slowness-container)

### **Steps to check for resource allocation issues which can cause job slowness**

* Make sure that the cluster to be used has enough resources by verifying the applications currently running in spark cluster, using Yarn UI. Another source of information about the resources being used by the Spark Executors is the Spark Application UI. In the Spark UI, select the Executors tab to display Summary and Detail views of the configuration and resources consumed by the executors. These views can help you determine whether to change default values for Spark executors for the entire cluster, or a particular set of job executions.
* Depending on your Spark workload, you may determine that a non-default Spark configuration provides more optimized Spark job executions. You should perform benchmark testing with sample workloads to validate any non-default cluster configurations. Some of the common parameters that you may consider adjusting are:

    * --num-executors sets the number of executors
    * --executor-cores sets the number of cores for each executor
    * --executor-memory controls the memory size (heap size) of each executor on Apache Hadoop YARN, and you'll need to leave some memory for execution overhead
    
* Following command is an example of how to change the configuration parameters for a batch application that is submitted using spark-submit: `spark-submit --class --executor-memory 3072M --executor-cores 4 –-num-executors 10`

