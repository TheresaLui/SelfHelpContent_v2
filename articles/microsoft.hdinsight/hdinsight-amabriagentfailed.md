<properties
    pageTitle="Cluster failure due to disk full on head node"
    description="Cluster failure due to disk full on head node"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="27"
    articleId="Hdi_DiskFull"
    diagnosticScenario="HDInsightAmbariAgentNotStartingInsight"
    selfHelpType="rca"
    supportTopicIds="32588422, 32588427"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high disk usage on the headnode. Please ssh into the headnode and clean up any files that you placed there that are not needed.

## **Recommended steps**
1. [SSH](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix) into the node

1. Run 'du -h --max-depth=1 /'

1. Clean up the largest files that you placed there