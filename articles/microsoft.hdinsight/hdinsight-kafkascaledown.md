<properties
    pageTitle="Kafka cluster cannot be scaled down"
    description="Kafka cluster cannot be scaled down"
    infoBubbleText="Found recent kafka cluster scale down failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-anreg"
    displayOrder="30"
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

Scale down of disks or nodes is not supported for any milestone. 

Kafka is a technology used for data ingestion and retention. 
Due to the storage heavy nature of the technology, it is not recommended to scale down Kafka clusters as customers risk data-loss. 

Due to this, scale down is explicitly disallowed on HDInsight Kafka.

## **Recommended steps**
Delete and recreate the cluster.

Please provide feedback at https://feedback.azure.com/forums/217335-hdinsight

