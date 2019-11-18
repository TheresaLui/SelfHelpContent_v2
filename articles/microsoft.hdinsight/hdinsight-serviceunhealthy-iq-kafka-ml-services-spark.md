<properties
    pageTitle="Azure HDInsight: Service Unhealthy"
    description="Azure HDInsight: Service Unhealthy"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-miegge"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636466,32636472,32636480,32636497"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
    articleId="f10eed21-c120-4722-bfad-1b46217cae9d"
/>

# Azure HDInsight: Service Unhealthy

## **Recommended Steps**

* If you're using a custom script action, review the logs associated with the script action to investigate whether they may be causing a problem. For more information on reviewing logs, see [Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting).
* If you made customizations to your cluster by installing additional libraries or modifying configurations or .jar files, your changes may have impacted the health and performance of the cluster. You may want to undo your modifications, or create a new cluster and test each modification as you go.
* If you are having issues with Ambari, try restarting it using the following command:

   sudo systemctl restart ambari-server

* If you're trying to reach links in the Ambari UI that are not exposed to the internet, such as JobTracker, you must [create an SSH tunnel with HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-linux-ambari-ssh-tunnel).

* If services that rely on Zookeeper nodes are failing to start, see [Zookeeper server fails to form a quorum](https://hdinsight.github.io/zookeeper/manage-zookeeper-snapshot.html).

* If jobs on the cluster are running slow or failing, follow the steps in [Troubleshoot a slow or failing job on a HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster).

Note that Microsoft Support teams can offer support only for the following situations:
* Issues or errors that occur when loading a custom script. Any errors that occur during the execution of custom scripts are outside the scope of a support ticket.
* Applications and libraries that are part the default cluster creation process.

## Recommended documents

* [Apache Ambari heartbeat issues in Azure HDInsight](https://review.docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues?branch=master)
* [Why does the Hive Zeppelin Interpreter give a Zookeeper error?](https://hdinsight.github.io/hive/hive-llap-zeppelin-namespace.html)
* [Livy Server fails to start with java.lang.OutOfMemoryError](https://hdinsight.github.io/spark/livy-nativethread-exhaustion.html)
* [java.lang.OutOfMemoryError: Java heap space error when trying to open spark history server](https://hdinsight.github.io/spark/spark-history-heap-memory-configuration.html)
* [Frequently asked questions about Apache Kafka in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/kafka/kafka-faq)
