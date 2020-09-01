<properties
    pageTitle="Azure HDInsight: Service Unhealthy"
    description="Azure HDInsight: Service Unhealthy"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-miegge"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636466,32636472,32636480"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
    articleId="f10eed21-c120-4722-bfad-1b46217cae9d"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight: Service Unhealthy

## **Recommended Steps**

The following steps may help you troubleshoot issues when a service running on HDInsight is down, won't start, or doesn't work as expected:

* If you made customizations to your cluster by installing additional libraries, modifying configurations or .jar files, your changes may have impacted the health and performance of the cluster. You may want to undo your modifications, or create a new cluster and test each modification as you go.
* If you're using a custom script action, review the logs associated with the script action to investigate whether they may be causing a problem. For more information, see [Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting).
* If you are having heartbeat issues with Ambari, see [Apache Ambari heartbeat issues](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues), or try restarting Ambari using the following command: sudo systemctl restart ambari-server
* If jobs on the cluster are running slow or failing, follow the steps in [Troubleshoot a slow or failing job](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster).
* If you recently enabled secure transfer on your Storage account and get the error "The account being accessed does not support http" you need to disable secure transfer, or make additional configuration changes as described in [Enable WASBS in HDInsight clusters](https://hdinsight.github.io/hdfs/wasbs-common-problems-regarding-to-wasbs.html).
* Please ensure that you are using the recommended NameNode sizes. If the NameNode size is smaller than the recommended size, you may encounter issues. See [Supported node configurations](https://docs.microsoft.com/azure/hdinsight/hdinsight-supported-node-configuration#all-supported-regions-except-brazil-south-and-japan-west) for more information. 

Note that Microsoft Support teams can offer support only for the following situations:

* Issues or errors that occur when loading a custom script. Any errors that occur during the execution of custom scripts are outside the scope of a support ticket.
* Applications and libraries that are part the default cluster creation process

## **Recommended Documents**

* [Frequently asked questions about Apache Kafka in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/kafka/kafka-faq)
* [Troubleshooting Interactive Query clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-hive-out-of-memory-error-oom)
