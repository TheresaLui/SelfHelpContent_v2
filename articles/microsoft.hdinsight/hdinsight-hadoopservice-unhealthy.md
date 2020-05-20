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
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="328b4e89-006b-481e-b12e-f700ca1938d7"
	ownershipId="AzureData_HDInsight"
/>
# Azure HDInsight: Services hosted on the Cluster are Failing to start
 
## **Recommended Documents**

* **Jobs Failing**: Use Ambari UI to check for resource issues if your jobs are fialing. Check if enough resources are available to process the submitted Applications, for around the time when the job was submitted.  When YARN Application is fully utilized, Application that are submitted will be queued in accepted state until resources are freed up to submit the jobs. A known side-effect of high memory usage is "Unable to submit any jobs". 

* If you are able to SSH to node and services are not reflecting correctly in Ambari UI, reboot Ambari Agent on the corresponding node using command: sudo service ambari-agent restart

* [**Services that rely on Zookeepers are failing to start-Zookeeper server fails to form a quorum**](https://hdinsight.github.io/zookeeper/manage-zookeeper-snapshot.html)

* [**Ambari Agent Heartbeat Lost**](https://hdinsight.github.io/ambari/ambari-agent-heartbeat-lost.html)

* [**Manage HDInsight clusters by using the Apache Ambari Web UI**](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari#management)

