<properties
    pageTitle="Ambari Alerts"
    description="Ambari Alerts"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="mimig1"
    ms.author="mimig"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636446, 32636449, 32636457, 32636462, 32636468, 32636478, 32636493, 32636499"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec, mooncake, blackforest"
    articleId="hdinsight-ambari-alert"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight: Ambari Alerts

## Recommended Steps

To resolve common issues, try one or more of the following steps.

* **Reboot your nodes.** If your node is unresponsiveness and/or you see a critical alert for a specific node, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).

* **Retry to see if the issue is transient.** Ambari heartbeat lost alerts are usually transient and will resolve on their own own. For more information about heartbeat issues, see [Apache Ambari heartbeat issues in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues).

* **Learn about alerts.** 
    * For an explanation of the type of alert statuses provided in Ambari, see [Alerts](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari#alerts).

    * Ambari stale alerts can be caused when the host is highly utilized or cluster is under heavy load. One way to mitigate this is to disable and enable the alert. For more information, see [Apache Ambari stale alerts in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-stale-alerts).

## **Recommended Documents**

Additional information is available in the following Hortonworks documents:

* [Managing Alerts and Notifications](https://docs.hortonworks.com/HDPDocuments/Ambari-2.7.3.0/managing-and-monitoring-ambari/content/amb_managing_alerts_and_notifications.html)
* [Description, potential causes and possible remedies for predefined alerts](https://docs.hortonworks.com/HDPDocuments/Ambari-2.7.3.0/managing-and-monitoring-ambari/content/amb_predefined_alerts.html)
