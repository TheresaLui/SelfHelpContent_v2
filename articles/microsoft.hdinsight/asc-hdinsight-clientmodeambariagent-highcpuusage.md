<properties
    pageTitle="Cluster Failure due to Spark application running in client mode"
    description="Cluster Failure due to Spark application running in client mode"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ravi"
    ms.author="v-ravikc"
    displayOrder=""
    articleId="Hdi_ClientModeAgentCpuUsage"
    diagnosticScenario="HDInsightClientModeAmbariAgentHighCpuUsageInsight"
    selfHelpType="rca"
    supportTopicIds="32636495, 32636496, 32636497, 32636498"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, mooncake, blackforest, fairfax"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high CPU usage on the headnode.
CPU Percent Used Memory <!--$PercentUsedMemory-->[PercentUsedMemory]<!--/$PercentUsedMemory-->
<!--issueDescription-->
## Problem

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high CPU usage on the headnode because of Spark applications running in client mode. Spark applications running in client mode utilize resources on the head node. Modifying the application to use cluster mode would reduce the stress on the head node and decrease head node loss.

## **Recommended Steps**

In order to reduce stress on the head node, please update the Spark applications running in client mode and change them to cluster mode using the following steps:

1. Identify the Spark applications running in client mode. The top resource consumers are listed below for reference.
1. Update the [Spark application deployment](https://spark.apache.org/docs/latest/submitting-applications.html#launching-applications-with-spark-submit) to use cluster mode by explicitly stating 'deploy-mode cluster' 

