<properties
    pageTitle="HDInsight cluster having HDFS checkpoint error"
    description="HDInsight cluster having HDFS checkpoint error"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    authorAlias="nebhatta"
    displayOrder="33"
    articleId="Hdi_Crud_Checkpoint"
    diagnosticScenario="HDInsightHdfsCheckpointInsight"
    selfHelpType="rca"
    supportTopicIds="32588504"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> checkpoint error

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is currently suffering from HDFS checkpoint error. 

## **Recommended steps**
* Log onto your HDInsight cluster

* Restart Ambari service using this command "sudo service ambari-agent restart" on the following nodes, note if the list is empty this step can be skipped  
<!--$listhosts-->[listhosts]<!--/$listhosts-->

* Once both Namenodes are running to get rid of the NameNode Last Checkpoint Alert run the following commands
  - hdfs dfsadmin -D 'fs.default.name=hdfs://<!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->/' -safemode enter
  - hdfs dfsadmin -D 'fs.default.name=hdfs://<!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->/' -saveNamespace
  - hdfs dfsadmin -D 'fs.default.name=hdfs://<!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->/' -safemode leave