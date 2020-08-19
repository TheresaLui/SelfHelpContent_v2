<properties
	pageTitle="Python SDK issues"
	description="Python SDK issues"
	infoBubbleText="Python SDK issues"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690872"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.workspace.python"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Python SDK issues

## **Recommended Steps**

If you are experiencing issues with the Python SDK, make sure you have the [latest version](https://pypi.org/project/azureml-sdk/) installed.

To check the currently installed version:

```
import azureml.core
print(azureml.core.VERSION)
```

Should an upgrade be needed, run the following command:

```
pip install --upgrade azureml-sdk
```

The SDK also contains several optional components (`extras`) that will only be installed if specified. Make sure you also have the latest versions of any optional components you are using.

```
pip install --upgrade azureml-sdk[explain,automl]
```

For a list of all the optional components, see the following [table](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py&viewFallbackFrom=azure-ml-py#advanced-install-extras).


## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [Install Azure Machine Learning Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py)
* [Azure Machine Learning Python SDK reference docs](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
