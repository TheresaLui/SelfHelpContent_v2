<properties
    pageTitle="Cluster failure due to disk full on head node"
    description="Cluster failure due to disk full on head node"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="27"
    articleId="Hdi_HighDiskUsage"
    diagnosticScenario="HDInsightDiskUsageInsight"
    selfHelpType="rca"
    supportTopicIds="32636428"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

## Problem

<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high disk usage on the headnode. Please ssh into the headnode and clean up any files that are not needed.
<!--/issueDescription-->

## **Recommended Steps**

* Cleaning the unwanted files:
	1. [SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix) into the node
	1. Run `du -h --max-depth=1 / | sort -h`
	1. Clean up the largest files that you placed there

* Setting the properties in Ambari dashboard:
	1. yarn.nodemanager.localizer.cache.target-size-mb=2048 
	1. yarn.nodemanager.localizer.cache.cleanup.interval-ms=300000
	
	Refer to the [document](https://hortonworks.com/blog/resource-localization-in-yarn-deep-dive/) for more details.	

### Nodes with high disk usage

<!--$NodeInformation-->[NodeInformation]<!--/$NodeInformation-->

## **Recommended Documents**

* [Cluster node out of disk space](https://hdinsight.github.io/ClusterManagement/cluster-node-out-of-disk-space.html#cluster-node-out-of-disk-space)
