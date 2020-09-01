<properties
    pageTitle="Kafka cluster cannot be scaled down"
    description="InvalidKafkaScaleDownIssue"
    infoBubbleText="Found recent Kafka cluster scale down failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Kafka_ScaleDownFailure"
    diagnosticScenario="HDInsightKafkaScaleDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32681539"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
On <!--$PreciseTimeStamp-->[PreciseTimeStamp]<!--/$PreciseTimeStamp--> an operation to scale down the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->
failed, as scaling down of nodes is not supported for HDInsight Kafka clusters.
<!--/issueDescription-->

Apache Kafka on HDInsight is a technology used for data ingestion and retention. Data is stored in each node of the cluster. Scaling down an HDInsight Kafka cluster would result in the removal of nodes from the cluster. All the data stored in the removed nodes will be lost.

To prevent data loss, **scale down operations are explicitly disallowed on HDInsight Kafka clusters**.

## **Recommended Steps**

The only way to reduce the size of an HDInsight Kafka cluster is to delete the existing cluster and create a new, smaller cluster.

## **Recommended Documents**

* [Getting started with HDInsight Kafka Cluster](https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-get-started)
* [Storage and Scalability for Apache Kafka on HDInsight](https://docs.microsoft.com/azure/hdinsight/kafka/apache-kafka-scalability)
