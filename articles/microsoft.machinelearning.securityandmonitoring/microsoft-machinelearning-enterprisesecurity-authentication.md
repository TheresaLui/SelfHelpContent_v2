<properties
	pageTitle="Authentication & Role Based Access (RBAC)"
	description="Authentication & Role Based Access (RBAC)"
	infoBubbleText="Authentication & Role Based Access (RBAC)"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690837"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.authentication"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Authentication & Role Based Access (RBAC)

An Azure Machine Learning workspace is an Azure resource. Like other Azure resources, when a new Azure Machine Learning workspace is created, it comes with three default roles. 

1. **Reader**: Read-only actions in the workspace. Readers can list and view assets in a workspace, but can't create or update these assets.
2. **Contributor**: View, create, edit, or delete (where applicable) assets in a workspace. For example, contributors can create an experiment, create or attach a compute cluster, submit a run, and deploy a web service.
3. **Owner**: Full access to the workspace, including the ability to view, create, edit, or delete (where applicable) assets in a workspace. Additionally, you can change role assignments.

If the built-in roles are insufficient, you can create custom roles. See the [following article](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) to learn more.

## **Recommended Steps**

Assuming you have been assigned access to the workspace through one of the RBAC roles, you can follow one the below methods to authenticate into it.

### **Interactive Authentication**

Most examples in the documentation follow the interactive authentication method using the Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py). Calling the `from_config()` function will issue a prompt to authenticate in a separate browser:

```
from azureml.core import Workspace
workspace = Workspace.from_config()
workspace.get_details()
```

The `from_config()` function looks for a JSON file containing your workspace connection information. If you are using an Azure Machine Learning [Compute Instance](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance), this should already exist in your file share. If you are using the SDK locally, you can create a file called `config.json` in the same directory with the following content"

```
{
    "subscription_id": "<YOUR SUBSCRIPTION ID>",
    "resource_group": "<YOUR RESOURCE GROUP>",
    "workspace_name": "<YOUR WORKSPACE NAME>"
}
```

### **Service Principal Authentication**

Service principal authentication allows you to authentication through automated workflows as it is not tied to a specific user. This can be done using the Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py) as follows:

```
from azureml.core.authentication import ServicePrincipalAuthentication
from azureml.core import Workspace

service_principal = ServicePrincipalAuthentication(tenant_id="<YOUR TENANT ID>", 
                                                   service_principal_id="<YOUR CLIENT ID>",
                                                   service_principal_password="<YOUR CLIENT SECRET>") 
workspace = Workspace.get(name="<YOUR WORKSPACE NAME", 
                          auth=service_principal,
                          subscription_id="<YOUR SUBSCRIPTION ID>")
workspace.get_details()
```

### **REST API Authentication**

A service principal can be used to authenticate using the Azure Machine Learning [REST API](https://docs.microsoft.com/rest/api/azureml/). The following Python code will generate an authentication token to your workspace resource (run `pip install adal` to download required package):

```
from adal import AuthenticationContext

client_id = "<YOUR CLIENT ID>"
client_secret = "<YOUR CLIENT SECRET>"
resource_url = "https://login.microsoftonline.com"
tenant_id = "<YOUR TENANT ID>"
authority = "{}/{}".format(resource_url, tenant_id)

auth_context = AuthenticationContext(authority)
token_response = auth_context.acquire_token_with_client_credentials("https://management.azure.com/", client_id, client_secret)
print(token_response)
```

## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [Setup authentication for Azure Machine Learning resources and workflows](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication)
* [Manage access to Azure Machine Learning workspace](https://docs.microsoft.com/azure/machine-learning/how-to-assign-roles)
* [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
