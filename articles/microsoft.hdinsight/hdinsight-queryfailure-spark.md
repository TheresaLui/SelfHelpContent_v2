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
    cloudEnvironments="public, MoonCake"
    articleId="302b8254-83e6-4005-9d2e-891f19ebc0f3"
/>

# Azure HDInsights Query Failure - Spark

## **Recommended Steps**

**Configuration Steps for Spark Applications**

* [How do I configure an Apache Spark application by using Apache Ambari on clusters?](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark#how-do-i-configure-an-apache-spark-application-by-using-apache-ambari-on-clusters)
* [How do I configure an Apache Spark application by using a Jupyter notebook on clusters?](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark#how-do-i-configure-an-apache-spark-application-by-using-a-jupyter-notebook-on-clusters)
* [How do I configure an Apache Spark application by using Apache Livy on clusters?](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark#how-do-i-configure-an-apache-spark-application-by-using-apache-livy-on-clusters)
* [How do I configure an Apache Spark application by using spark-submit on clusters?](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark#how-do-i-configure-an-apache-spark-application-by-using-spark-submit-on-clusters)
* [Use Apache Spark REST API to submit remote jobs to an HDInsight Spark cluster](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-livy-rest-interface)

**Troubleshooting**

* [Troubleshoot a slow or failing job on a HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster)
* [Debug Apache Spark jobs running on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-job-debugging)
* [Use extended Apache Spark History Server to debug and diagnose Apache Spark applications](https://docs.microsoft.com/azure/hdinsight/spark/apache-azure-spark-history-server)
* [Debug Apache Spark applications locally or remotely on an HDInsight cluster with Azure Toolkit for IntelliJ through SSH](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-intellij-tool-debug-remotely-through-ssh)
* [Troubleshoot Apache Hadoop YARN by using Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-yarn)

**Spark Application Failed with OutOfMemoryError**

* Determine the maximum size of the data the Spark application will handle. A guess can be made based on the maximum of the size of input data, the intermediate data produced by transforming the input data, and the output data produced further transforming the intermediate data. This can also be an iterative process, if an initial guess is not possible.

* Make sure that the HDInsight cluster to be used has enough resources (memory and cores) to accommodate the Spark application. This can be determined by viewing the Cluster Metrics section of the YARN UI of the cluster for the values of Memory Used vs. Memory Total, and VCores Used vs. VCores Total.

* Set the Spark configurations to appropriate values that do not exceed 90% of the available memory and cores as viewed by YARN, yet well within the memory requirement of the Spark application.

**Issues with YARN applications**

To solve issues with YARN applications, the following articles might be helpful:

* **YARN Timeline Server**: The YARN Timeline server provides generic information on completed applications and framework-specific application information
* **YARN Application logs**: The application logs can be useful in debugging issues, with aggregated logs being stored in the path `/app-logs/<user>/logs/<applicationId>`
* **YARN CLI tools**: After connecting to HDInsight cluster using SSH, the YARN logs can be collected using `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>`
* **YARN ResourceManager UI**: Add `/yarnui/hn/logs/` to the end of the cluster URL to view the YARN logs

## **Recommended Documents**

* [Access YARN application logs on Linux-based HDInsight](https://docs.azure.cn/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)
* [How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)
* [Spark Application Failed with OutOfMemoryError](https://hdinsight.github.io/spark/spark-application-failure-with-outofmemoryerror.html)
