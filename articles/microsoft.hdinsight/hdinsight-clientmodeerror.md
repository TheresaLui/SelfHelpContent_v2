<properties
    pageTitle="Cluster Failure due to Spark Application running in Client Mode"
    description="Cluster Failure due to Spark Application running in Client Mode"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder=""
    articleId="Hdi_Ambari_ClientMode"
    selfHelpType="resource"
    supportTopicIds=""
    diagnosticScenario=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

We noticed that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high CPU usage on the headnode because of Spark Applications running in client mode.

## Applications in Client Mode
<!--$Parameters-->[Parameters]<!--/$Parameters-->

## **Recommended steps**
In order to reduce stress on the head node please update the Spark Applications running in Client Mode and change them to Cluster mode using the following steps:

1. Identify the Spark Applications running in Client Mode

1. Update the [Spark Application Deployment](https://spark.apache.org/docs/latest/submitting-applications.html#launching-applications-with-spark-submit) to use cluster mode by explictly stating 'deploy-mode cluster' 

1. Restart the gateway node for the action to take effect.