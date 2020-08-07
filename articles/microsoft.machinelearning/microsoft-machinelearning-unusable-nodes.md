<properties
    pageTitle="Cluster or Instance has unusable nodes"
    description="Article on Training Cluster or Compute Instance having unusable node issues"
    service="microsoft.machinelearning"
    resource="Microsoft.MachineLearningServices/workspaces/computes"
    authors="nishankgu"
    ms.author="nigup"
    selfHelpType="generic"
  articleId="microsoft-machinelearning-unusable-nodes.md"
    supportTopicIds="32690843"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# When clusters or instances have unusable nodes

This helps users diagnose unusable nodes in a training cluster or when the compute instance goes into an unusable state at the time of creation. This article does not help if your compute instance goes into unusable state after stopping and starting the instance again. Please create a technical support ticket in that case.

## **Recommended Steps**

1. In case of compute clusters try waiting for the compute to recycle the unusable nodes. It generally takes about an hour for that to happen, and improvements are being made to reduce this time further.
2. If you get unusable node while trying to deploy compute instance behind vnet make sure to check your NSG rules at subnet level per [this documentation](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#compute-instance)
3. If there are no other jobs running on that compute or you created this instance for the first time, try to delete and recreate the compute using the same or another name.
4. Check to see if there is an error on the compute that tells you the reason on why it is in an unusable state. Some common issues here include:
* Disk being full on the node from a previous job resulting in the node being unable to run another job
* Incorrect network setup that prevents Azure to communicate with the node after being provisioned
* Azure not having sufficient capacity for that VM Size in that region, especially if you are using GPUs
5. If your instance switches to Unusable state later while using, try to restart your compute instance. If this issue persists please try to switch to higher Core/Mem VM Size. 
6. If the problem persists, please create a support ticket

## **Recommended Documents**

* [Learn more about setting up your VNet for managed compute](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#compute)
