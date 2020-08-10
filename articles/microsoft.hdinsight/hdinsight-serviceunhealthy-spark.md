<properties
    pageTitle="Service Unhealthy Spark Update 2.7"
    description="Service Unhealthy Spark Update 2.7"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-miegge"
    ms.author="jaserano"
    selfhelptype="generic"
    articleId="44469f33-c07e-4566-a098-2268afdebd8a"
    supportTopicIds="32636497"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# Service Unhealthy, Spark Update 2.7

## Recommended Steps

**Reboot your nodes.** If your node is unresponsiveness and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).

**Ambari issues**

* Heartbeat Lost: If you are having heartbeat issues with Ambari, see [Apache Ambari heartbeat issues](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues)
* Ambari DB Connection Limit reached:

  * **Cause**: Multiple Hive queries running in parallel or too many nodes
  * **Solution**: Because the Ambari database included with a cluster is not configurable, it is recommended that you can [configure your own custom Ambari Database](https://docs.microsoft.com//azure/hdinsight/hdinsight-custom-ambari-db) to match the size of the node and the number of queries that are submitted in parallel. This also allows you the flexibility to have a view of your own Ambari Database.

**Jobs on cluster are slow or failing**

* If jobs on the cluster are running slow or failing, follow the steps in [Troubleshoot a slow or failing job](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster)

**Hive is down**

* If you find that Hive is down, check if the HiveServer2 is stopped on both the headnodes and start hiveserver2 from Ambari UI

**My Cluster is in SafeMode**

* If your cluster is stuck in SafeMode, please follow the [Cluster stuck in SafeMode troubleshooting guide](https://docs.microsoft.com//azure/hdinsight/hadoop/hdinsight-hdfs-troubleshoot-safe-mode)

**Jupyter notebook issues**

* Updating Anaconda and Python are not supported for Juptyer. [Please ensure that you have the baseline versions of 3.5 and 2.7](https://docs.microsoft.com//azure/hdinsight/spark/apache-spark-python-package-installation#understand-default-python-installation) are the baselines and versions should not be upgraded to any future versions than 3.5 and 2.7.
* **Note**: If customers would like to upgrade files the only supported option is to [create a new environment](https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/hdinsight/spark/apache-spark-python-package-installation.md)

**Customizations**

* If you made customizations to your cluster by installing additional libraries, modifying configurations or .jar files, your changes may have impacted the health and performance of the cluster. You may want to undo your modifications or create a new cluster and test each modification as you go.
* **Note**: Microsoft Support teams can offer support only for applications and libraries that are part the default cluster creation process

**Custom Script Actions**

* If you're using a custom script action, review the logs associated with the script action to investigate whether they may be causing a problem. For more information, see [Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting).
* **Note**: Microsoft Support teams can offer support only for issues or errors that occur when loading a custom script. Any errors that occur during the execution of custom scripts are outside the scope of a support ticket.

**Error: The account being accessed does not support http**

* If you recently enabled secure transfer on your Storage account and receive the error above, you need to disable secure transfer, or make additional configuration changes as described in [Enable WASBS in HDInsight clusters](https://hdinsight.github.io/hdfs/wasbs-common-problems-regarding-to-wasbs.html)

## **Recommended Documents**

* [Troubleshoot Apache Spark by using Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/spark/apache-troubleshoot-spark)
* [Known Issues for Apache Spark Clusters](https://docs.microsoft.com/azure/hdinsight/spark/apache-spark-known-issues)
