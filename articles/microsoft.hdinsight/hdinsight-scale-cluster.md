<properties
    pageTitle="Scale HDInsight Cluster"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636492"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-scale-cluster"
/>

# Scale HDInsight Cluster

## Most Common HDInsight Scale Issues

The following are the most common issues encountered when scaling HDInsight.

### The maximum number of deployments in a resource group has been reached

Azure has a quota limit of 800 deployments per resource group. Scale deployments will fail when we hit this limit. Since the customer's HDInsight cluster resource resides in their resource group, in their resource subscription, and the actual cluster assets reside in our provisioning subscriptions in its own resource group, the issue can happen when we hit the limit in either of the resource groups.

1. From the portal, sign into the portal and navigate to your resource group

1. Select **Deployments** from the resource group. If this count shows that it has reached the limit, delete old deployments to fix the issue. You can safely delete all deployments that are "X" days old. "X" can be 30 or so based on how frequent deployments happen in this resource group.

### Not enough cores available

Customers will attempt to scale a cluster during the scale operation. However, during this operation, the customer will have fewer cores available in the subscription than what is needed for the scale operation. Please ensure that you have enough available cores. If you do not have enough available cores, [follow these steps](https://docs.microsoft.com/azure/hdinsight/hdinsight-capacity-planning#quotas).

### Operations Management Suite (OMS) is enabled and blocking the ability to scale

Customers have experienced issues with scale-up operations failing during an OMS script installation. This is a known issue. If you have OMS enabled, please disable OMS temporarily, scale-up the cluster, then re-enable OMS.

### Missing Required IP

If you use either network security groups or user defined routes to control traffic, you must allow traffic from the IP addresses used by Azure Health and Management services, so that they can communicate with your HDInsight cluster.

Some of the IP addresses are region specific, while others apply to all Azure regions. You may also need to allow traffic from the Azure DNS service if you aren't using custom DNS. [Click here for the list of required IPs](https://docs.microsoft.com/azure/hdinsight/hdinsight-management-ip-addresses).

### Not enough IP addresses

HDInsight cluster scaling can fail if the subnet in which this HDInsight cluster is deployed does not have a sufficient number of free IP addresses, to match the number of nodes that you need to scale-up the cluster.

To create space on the virtual network, please do one of the three steps below:

1. Delete unused resources within the subnet, opening up IP addresses that can be used for the cluster scaling
1. Add a subnet and create a new HDInsight cluster within the newly created subnet
1. Change the subnet settings to the existing virtual network, to include a larger address space

### Additional Information

* HDInsight does not allow you to upgrade worker node disk sizes on a running cluster. Currently, you must choose the disk size when the cluster is created. HDInsight clusters are designed to be easily dropped and re-created.
* It is recommended that you scale down HDInsight to a minimum of three worker nodes. For Kafka, you cannot scale down the worker nodes.
* Scaling your HDInsight is not possible via ARM templates. You can scale your cluster using five different methods:<br>

    * PowerShell Az
    * PowerShell AzureRM
    * Azure CLI
    * Azure Classic CLI
    * Azure portal
    
* Customers can enable auto-scale only during when creating a cluster. If you have not configured auto-scale when creating a cluster, you must delete the cluster, and create a new cluster with auto-scale enabled.

## **Recommended Documents**

* [Scale HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-scaling-best-practices)<br>
* [Automatically scale Azure HDInsight clusters (preview)](https://docs.microsoft.com/azure/hdinsight/hdinsight-autoscale-clusters?toc=%2F%2Fazure%2Fhdinsight%2Fhadoop%2FTOC.json&bc=%2F%2Fazure%2Fbread%2Ftoc.json)
