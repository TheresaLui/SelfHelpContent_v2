<properties
    pageTitle="Azure HDInsights: Hadoop Service Unhealthy"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636448"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec, blackforest, mooncake"
    articleId="328b4e89-006b-481e-b12e-f700ca1938d7"
	ownershipId="AzureData_HDInsight"
/>
# Azure HDInsight: Services hosted on the cluster are failing to start

## Recommended Steps

To resolve common issues, try one or more of the following steps.

* **Reboot your nodes.** If your node is unresponsiveness and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).

* **Check for failed jobs**: Use Ambari UI to check for resource issues if your jobs are failing. Check if enough resources are available to process the submitted Applications, for around the time when the job was submitted.  When the YARN application is fully utilized, applications that are submitted will be queued in an accepted state until resources are freed up to submit the jobs. A known side-effect of high memory usage is "Unable to submit any jobs".

* **Reboot Ambari.** If you are able to SSH to node and services are not reflecting correctly in Ambari UI, reboot the Ambari Agent on the corresponding node using the following command: ```sudo service ambari-agent restart```

## **Recommended Documents**

* [**Services that rely on Zookeepers are failing to start-Zookeeper server fails to form a quorum**](https://hdinsight.github.io/zookeeper/manage-zookeeper-snapshot.html)

* [**Ambari Agent Heartbeat Lost**](https://hdinsight.github.io/ambari/ambari-agent-heartbeat-lost.html)

* [**Manage HDInsight clusters by using the Apache Ambari Web UI**](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari#management)

