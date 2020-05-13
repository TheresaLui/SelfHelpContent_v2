<properties
    pageTitle="Cluster Failure due to Spark application running in client mode"
    description="Cluster Failure due to Spark application running in client mode"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="25"
    articleId="Hdi_Ambari_ClientMode"
    diagnosticScenario="HDInsightClientModeInsight"
    selfHelpType="rca"
    supportTopicIds="32636423"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

## Problem
<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high CPU usage on the headnode because of Spark applications running in client mode. Spark applications running in client mode utilize resources on the head node. Modifying the application to use cluster mode would reduce the stress on the head node and decrease head node loss.
<!--/issueDescription-->

## **Recommended Steps**

In order to reduce stress on the head node, please update the Spark applications running in client mode and change them to cluster mode using the following steps:

1. Identify the Spark applications running in client mode. The top resource consumers are listed below for reference.
1. Update the [Spark application deployment](https://spark.apache.org/docs/latest/submitting-applications.html#launching-applications-with-spark-submit) to use cluster mode by explicitly stating 'deploy-mode cluster' 

## Applications running in client mode
<!--$Parameters-->[Parameters]<!--/$Parameters-->
