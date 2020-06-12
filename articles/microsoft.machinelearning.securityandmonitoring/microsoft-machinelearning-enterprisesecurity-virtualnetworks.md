<properties
	pageTitle="Virtual Network Configuration"
	description="Virtual Network Configuration"
	infoBubbleText="Virtual Network Configuration"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32740868"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.virtualnetwork"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Virtual Network Configuration

## **Recommended Steps**

A virtual network acts as a security boundary, isolating your Azure resources from the public internet. To ensure your workspace, training jobs, and inferencing jobs all remain secured behing a virtual network, the follow steps should be taken:

1. Ensure your workspace is behind an Azure Private Link, which enables you to connect to your workspace using a private endpoint. This will limit access to your workspace to only occur over a set of private IP addresses inside your virtual network.
2. Ensure all other Azure resources associated with your workspace are created within a virtual network (storage accounts, compute targets, key vaults etc).

### **Setup Private Link on Workspace**

For instructions on how to create and use a private link enabled workspace, see the following [article](https://docs.microsoft.com/azure/machine-learning/how-to-configure-private-link).

### **Setup Virtual Network on Associated Azure Resources**

For instructions on how to ensure all your associated resources are created behind virtual networks, see the following [article](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network).

## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [Azure Private Link Overview](https://docs.microsoft.com/azure/private-link/private-link-overview)
* [Azure Virtual Networks Overview](https://docs.microsoft.com/azure/virtual-network/virtual-networks-overview)
* [Azure Machine Learning Enterprise Security Overview](https://docs.microsoft.com/azure/machine-learning/concept-enterprise-security)
