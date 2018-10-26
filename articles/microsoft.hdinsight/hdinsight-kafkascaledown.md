<properties
    pageTitle="Kafka cluster cannot be scaled down"
    description="InvalidKafkaScaleDownIssue"
    infoBubbleText="Found recent Kafka cluster scale down failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_Kafka_ScaleDownFailure"
    diagnosticScenario="HDInsightKafkaScaleDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32588504, 32574297"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

<!--issueDescription-->
On <!--$TimeStamp-->[TimeStamp]<!--/$TimeStamp--> an operation to scale down the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> 
failed as scaling down of disks or nodes is not supported for HDInsight Kafka clusters.
<!--/issueDescription-->

Apache Kafka on HDInsight uses Azure Managed Disks. Since Kafka is very I/O heavy, Azure Managed Disks are used to provide high throughput and provide more storage per node. 
If traditional virtual hard drives (VHD) were used for Kafka, each node is limited to 1 TB. With managed disks, you can use multiple disks to achieve 16 TB for each node in the cluster. 
Reducing the number of nodes will lead to data loss on the managed disk attached to the nodes.

To prevent data loss, **scale down operations are explicitly disallowed on HDInsight clusters**. 




## **Recommended steps**

The only way to reduce the size of a cluster is to delete the existing cluster and create a new, smaller cluster. 


## **Recommended Documents**
[Getting started with HDInsight Kafka Cluster](https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-get-started)

[Storage and Scalability for Apache Kafka on HDInsight](https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-scalability)