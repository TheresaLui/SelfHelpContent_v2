<properties
    pageTitle="Cluster or Instance does not scale up"
    description="Article on Training Cluster scale up issues or Compute Instance start issues"
    service="microsoft.machinelearning"
    resource="Microsoft.MachineLearningServices/workspaces/computes"
    authors="nishankgu"
    ms.author="nigup"
    selfHelpType="generic"
  articleId="microsoft-machinelearning-cluster-scale-up-issues.md"
    supportTopicIds="32690842"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# When clusters or instances don't scale up

This helps users diagnose some common issues they might be facing when their cluster or compute instance does not scale up. This is helpful to diagnose issues when the compute has been created but it is not provisioning any nodes or the instance is not starting after creation.

## **Recommended Steps**

1. Check if you have enough quota by going to the "Quotas + Usages" section in your workspace for the region you are experiencing this issue in. It is possible that you don't have sufficient quota for that VMsize.
2. Check if you have an error on the compute by clicking on the Information icon on the portal or by calling the get_status() method in the SDK
3. Check to see if there is capacity in the Azure region that you are trying to create this compute in. It is possible that either the region is out of capacity or your VMsize is not supported in that region.
4. Check to see if there are any network setup issues that are preventing Azure to connect with the node. For example your NSG or firewall rules could be preventing the nodes to scale up.

## **Recommended Documents**

* [Learn how to view your quota](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#view-your-usage-and-quotas)
* [View supported regions for various VMsizes](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines)
* [Learn more about setting up your VNet for managed compute](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#compute)
