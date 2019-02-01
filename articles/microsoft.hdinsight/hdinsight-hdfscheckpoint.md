<properties
    pageTitle="HDInsight cluster having HDFS checkpoint error"
    description="HDInsight cluster having HDFS checkpoint error"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="33"
    articleId="Hdi_Health_Checkpoint"
    diagnosticScenario="HDInsightHdfsCheckpointInsight"
    selfHelpType="rca"
    supportTopicIds="32628986, 32629101"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> checkpoint error

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is currently suffering from HDFS checkpoint error. 

## **Recommended steps**
* Log onto your HDInsight cluster

* Restart Ambari service, on the nodes listed below, using this command :  
  *sudo service ambari-agent restart*  
  Note : If the following list is empty this step can be skipped  
  <!--$listhosts-->[listhosts]<!--/$listhosts-->

* Once both Namenodes are running, please run the following commands to reset the checkpoint :
  - hdfs dfsadmin -safemode enter
  - hdfs dfsadmin -saveNamespace
  - hdfs dfsadmin -safemode leave