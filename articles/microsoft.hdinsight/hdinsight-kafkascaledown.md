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

<!--issueDescription-->
## Problem

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed to scale down on <!--$TimeStamp-->[TimeStamp]<!--/$TimeStamp-->.

Scaling down of disks or nodes is not supported for Kafka clusters with managed disks. 

Apache Kafka is a technology used for data ingestion and retention. 
Due to the storage heavy nature of the technology, it is not recommended to scale down Kafka clusters as customers risk data-loss. 

Due to this, scaling down a cluster is explicitly disallowed on HDInsight Kafka.

Visit https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-scalability for storage and scalability configuration for Kafka on HDInsight.
<!--/issueDescription-->

## **Recommended steps**

The issue can be resolved by deleting the existing cluster and creating a new cluster with desired configuration. 
Refer https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-get-started for getting started with HDInsight Kafka Cluster.

Please provide feedback at https://feedback.azure.com/forums/217335-hdinsight

