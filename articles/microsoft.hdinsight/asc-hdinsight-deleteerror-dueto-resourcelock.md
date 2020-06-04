<properties
    pageTitle="Cluster deletion failure due to resource locks"
    description="Cluster deletion failure due to locks on cluster resources"
    infoBubbleText="Found recent cluster deletion failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    ms.author="ansiva"
    displayOrder="24"
    articleId="Hdi_DeleteError_ResourceLock"
    diagnosticScenario="HDInsightClusterDeleteErrorInsight"
    selfHelpType="rca"
    supportTopicIds="32681536"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

## Problem
<!--issueDescription-->
The cluster delete operation for <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed because there are locks on some of the resources in its resource group.

Since the delete did not succeed, a new cluster with the same name cannot be created in the same vNet.
<!--/issueDescription-->

## Locked Resources
<!--$LockedResources-->[LockedResources]<!--/$LockedResources-->

## **Recommended Steps**

The locks on the above resources need to be removed before the delete can succeed. Please refer to [Using Azure Resource Locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources) for instructions to remove these locks.

Once this is done, please notify Azure support and we will clean up the HDInsight cluster.
