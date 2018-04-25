<properties
    pageTitle="Cluster deletion failure due to resource locks"
    description="Cluster deletion failure due to locks on cluster resources"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="24"
    articleId="Hdi_DeleteError_ResourceLock"
    selfHelpType="resource"
    supportTopicIds="32511166, 32588502, 32588503"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Cluster Creation Fails Saying the Cluster Name is Already in Use.

## Problem
The cluster delete operation for <!--$ClusterDnsName--> ClusterDnsName <!--/$ClusterDnsName--> failed because there are locks on some of the resources in its resource group.

Since the delete did not succeed, a new cluster with the same name cannot be created in the same vNet.

## Locked Resources
<!--$LockedResources--> LockedResources <!--/$LockedResources-->  

## Recommended Mitigation Steps
The locks on the above resources need to be removed before the delete can succeed. Please refer to [Using Azure Resource Locks](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-lock-resources) for instructions to remove these locks.

Once this is done, please notify Azure support, and we will clean up the HDInsight cluster.
