<properties
	pageTitle="Problem provisioning or managing workspace"
	description="Problem provisioning or managing workspace"
	infoBubbleText="Problem provisioning or managing workspace"
	service="microsoft.machinelearning.workspace"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690836"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.workspace.manage"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem provisioning or managing workspace

## **Recommended Steps**

### **Azure Machine Learning Python SDK**

To create a workspace using the Python SDK:

```
from azureml.core import Workspace

workspace = Workspace.create(name='<WORKSPACE-NAME>',
                            subscription_id='<AZURE-SUBSCRIPTION-ID>',
                            resource_group='<RESOURCE-GROUP>',
                            create_resource_group=True,
                            location='<LOCATION>')
```

If a workspace has already been created, directly connect to the workspace:

```
from azureml.core import Workspace

workspace = Workspace.get(name='<WORKSPACE-NAME>',
                        subscription_id='<AZURE-SUBSCRIPTION-ID>',
                        resource_group='<RESOURCE-GROUP>')
```

Once access has be granted to the workspace, use any of the existing methods to manage and configure it. Refer to the following [documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.workspace.workspace?view=azure-ml-py) for additional reference.

### **Azure Machine Learning CLI**

To create a workspace using the CLI:

```
az ml workspace create -w <WORKSPACE-NAME> -g <RESOURCE-GROUP>
```

If a workspace has already been created, use the following command to list the details of your existing workspace:

```
az ml workspace list
```

Once the workspace has been created or workspace details have been retrieved, use the other existing CLI commands to manage and configure it. Refer to the following [documentation](https://docs.microsoft.com/cli/azure/ext/azure-cli-ml/ml/workspace?view=azure-cli-latest) for additional reference.

## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [What is an Azure Machine Learning workspace](https://docs.microsoft.com/azure/machine-learning/concept-workspace)
* [Azure Machine Learning Python SDK reference docs](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
* [Create and manage workspace using Azure CLI](https://docs.microsoft.com/azure/machine-learning/how-to-manage-workspace-cli)
* [Azure Machine Learning CLI reference docs](https://docs.microsoft.com/cli/azure/ext/azure-cli-ml/?view=azure-cli-latest)
