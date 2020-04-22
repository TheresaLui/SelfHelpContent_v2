<properties
	pageTitle="Accessing data behind virtual network"
	description="Creating datastores and datasets from storage behind virtual network"
	service="microsoft.machinelearning"
	resource="datasets"
	authors="sihhu"
	ms.author="sihhu"
	selfHelpType="generic"
	supportTopicIds="32690860"
	resourceTags=""
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleid="machinelearning-dataset-vnet"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Accessing data behind virtual network

Most users are able to learn how to create datastores and datasets from storage behind vitual network using the steps below:

## **Recommended Steps**

1. If your storage account is behind vNET, you can create datastores via SDK **only**. Learn [how to create datastores](https://docs.microsoft.com/azure/machine-learning/how-to-access-data#python-sdk).
2. To create Azure machine learning datasets, you can do so via either SDK or UI. Be sure to skip validation during dataset creation. This bypasses the initial validation check and ensures that you can create your dataset from these secure files. Learn [how to create datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets#create-datasets).

## **Recommended Documents**

* [Connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Create Azure Machine Learning datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)