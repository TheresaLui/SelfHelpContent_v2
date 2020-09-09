<properties
    pageTitle="HDInsight cluster deployment issue with Autoscaling"
    description="HDInsight cluster deployment issue with Autoscaling"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32681538"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9651a650-909c-4f84-a526-cb7ed6313e0b"
	ownershipId="AzureData_HDInsight"
/>

# HDInsight cluster deployment issue with Autoscaling

The Azure HDInsight Autoscale feature was released for general availability on November 7th, 2019 for Spark and Hadoop clusters and included improvements not available in the preview version of the feature. If you created a Spark cluster prior to November 7th, 2019 and want to use the Autoscale feature on your cluster, the recommended path is to create a new cluster, and enable Autoscale on the new cluster.

Autoscale for Interactive Query (LLAP) and HBase clusters is still in preview. Autoscale is only available on Spark, Hadoop, Interactive Query, and HBase clusters.

**Error: The deployment would exceed the quota of '800'.**

Azure has a quota limit of 800 deployments per resource group. Quotas are applied per resource group, subscriptions, accounts, and other scopes. For example, your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a virtual machine with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

To resolve this issue, delete the deployments that are no longer needed by using Azure portal, CLI or PowerShell. For more information, see [Resolve errors for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors).

**Error: the maximum node exceeded the available cores in this region**

Your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a resource with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

To request a quota increase, see [Create a support ticket to increase core](https://docs.microsoft.com/azure/hdinsight/hdinsight-capacity-planning#quotas).

**Operations Management Suite (OMS) is enabled and blocking the ability to scale**

The scale up operation will fail during an OMS script installation. This is a known issue. If you do have OMS enabled,  disable OMS temporarily, then scale up the cluster, then enable OMS.

**Azure health and management services is blocked in network security groups or user defined route**

If you use network security groups or user defined routes to control inbound traffic to your HDInsight cluster, you must ensure that your cluster can communicate with critical Azure health and management services. For more information, see [HDInsight management IP addresses](https://docs.microsoft.com/azure/hdinsight/hdinsight-management-ip-addresses
).

**Scaling failed because the HDInsight cluster subnet does not have sufficient free IP addresses to match the number of nodes you would like to scale up the cluster**

To resolve this issue, use one of the following methods:

- Delete unused resources within the subnet to release IP addresses
- Change the IP range of subnet settings for large available addresses
- Add a subnet and create a new HDInsight cluster within the newly created subnet

**Additional information**

1. HDInsight doesn't allow you to upgrade worker node disk sizes on a running cluster. Currently, you can choose the disk size when you create the cluster. HDInsight clusters are designed to be easily dropped and re-created.
2. It is recommended to scale down HDInsight to three worker nodes at least. For Kafka you cannot scale down the worker nodes.  
3. You can enable auto scale only when you create the cluster. If you have not configured auto scale during the creation, you must delete the cluster and recreate a cluster with autoscale enabled.

## **Recommended Documents**

* [Automatically scale Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-autoscale-clusters)
