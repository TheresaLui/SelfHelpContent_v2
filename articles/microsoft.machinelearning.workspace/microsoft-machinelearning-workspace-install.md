<properties
	pageTitle="Can't install or update SDK or CLI"
	description="Can't install or update SDK or CLI"
	infoBubbleText="Can't install or update SDK or CLI"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690840"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.workspace.install"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can't install or update SDK or CLI

## **Recommended Steps**

### **Azure Machine Learning Python SDK**

To install the default packages, run the following command.

```
pip install --upgrade azureml-sdk
```

The SDK contains several optional components (`extras`) that will only be installed if specified. To install the SDK with `extras`, append the component name(s) in brackets onto the default install. 

For example, the following command installs the SDK with the `explain` and `automl` variants.

```
pip install --upgrade azureml-sdk[explain,automl]
```

For a list of all the optional components, see the following [table](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py#advanced-install-extras).

### **Azure Machine Learning CLI**

To use the Azure Machine Learning CLI, the Azure CLI must first be installed. Follow the instructions [here](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) to do so.

Once the Azure CLI has been installed, the Machine Learning extension can be installed using the following command.

```
az extension add -n azure-cli-ml
```

### **Compute Instance**

As an alternative to installing the SDK or CLI locally, an Azure Machine Learning compute instance can be used instead. Compute instances are fully-managed cloud-based workstations designed for data scientists and comes with both the Python SDK and CLI pre-installed. Additionally, these instances also come pre-installed with common machine learning libraries such as PyTorch and Tensorflow. 

For more information, see the following [document](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance).

## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [Azure Machine Learning Python SDK install guide](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py)
* [Azure Machine Learning Python SDK reference docs](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
* [Azure Machine Learning CLI overview](https://docs.microsoft.com/azure/machine-learning/reference-azure-machine-learning-cli)
* [Azure Machine Learning CLI reference docs](https://docs.microsoft.com/cli/azure/ext/azure-cli-ml/?view=azure-cli-latest)
