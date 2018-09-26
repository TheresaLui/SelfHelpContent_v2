<properties
    pageTitle="Cluster Failure due to Spark application running in client mode"
    description="Cluster Failure due to Spark application running in client mode"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="25"
    articleId="Hdi_Ambari_ClientMode"
    diagnosticScenario="HDInsightClientModeInsight"
    selfHelpType="rca"
    supportTopicIds="32588427, 32588422, 32588445"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high CPU usage on the headnode because of Spark applications running in client mode. Spark application running in client mode utilizes resources on the head node. Modifying the application to use cluster mode would reduce the stress on the head node and decrease head node loss.

## **Recommended steps**
In order to reduce stress on the head node please update the Spark Applications running in client mode and change them to cluster mode using the following steps:

1. Identify the Spark Applications running in client mode, top offenders listed below

1. Update the [Spark application deployment](https://spark.apache.org/docs/latest/submitting-applications.html#launching-applications-with-spark-submit) to use cluster mode by explictly stating 'deploy-mode cluster' 

## Applications running in client mode
<!--$Parameters-->[Parameters]<!--/$Parameters-->