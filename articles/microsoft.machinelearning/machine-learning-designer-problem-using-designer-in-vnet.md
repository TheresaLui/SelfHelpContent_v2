<properties
	pageTitle="Problem using designer in virtual network"
	description="Problem using designer in virtual network"
	infoBubbleText="Problem using designer in virtual network"
	service="microsoft.machinelearning"
	resource="designer"
	authors="likebupt"
	ms.author="keli19"
	articleId="machine-learning-designer-problem-using-designer-in-vnet"
	selfHelpType="generic"
	supportTopicIds="32789518"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem using designer in virtual network

Follow these steps if you're having issues using Azure Machine Learning designer in a virtual network.

## **Recommended Steps**

- To use designer in the VNet, make sure you've followed [this article](https://docs.microsoft.com/azure/machine-learning/how-to-enable-studio-virtual-network) to configure your workspace.
- To use compute target in a virtual network, make sure you have met all requirements mentioned in [this article](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet) about how to secure training environments with virtual network. 
- If your workspace is behind VNet, you must put compute cluster and storage account in the same VNet. Additionally, use [private link](https://docs.microsoft.com/azure/machine-learning/how-to-configure-private-link?tabs=azure-portal#using-a-workspace-over-a-private-endpoint) to connect to the workspace.


## **Recommended Documents**

* [What is Azure Machine Learning designer?](https://docs.microsoft.com/azure/machine-learning/concept-designer)
* [Virtual network overview](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview)
* [Secure the workspace](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet)
* [Secure training environment](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet)
* [Secure the inferencing environment](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet) 
* [Use studio in virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-enable-studio-virtual-network)
