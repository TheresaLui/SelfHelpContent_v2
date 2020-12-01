<properties
  pagetitle="Authentication &amp; Role Based Access (RBAC)"
  service="microsoft.machinelearning"
  resource="machinelearning"
  ms.author="johwu"
  selfhelptype="Generic"
  supporttopicids="32690837"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.enterprisesecurity.authentication"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Authentication & Role Based Access (RBAC)

An Azure Machine Learning workspace is an Azure resource. Like other Azure resources, when a new Azure Machine Learning workspace is created, it comes with three default roles which can be assigned to users.

1. **Reader**: Read-only actions in the workspace. Readers can list and view assets in a workspace, but can't create or update these assets.
2. **Contributor**: View, create, edit, or delete (where applicable) assets in a workspace. For example, contributors can create an experiment, create or attach a compute cluster, submit a run, and deploy a web service.
3. **Owner**: Full access to the workspace, including the ability to view, create, edit, or delete (where applicable) assets in a workspace. Additionally, you can change role assignments.

When changing role assignments, it may take up to 30 minutes for them to take effect, as application caches are used to improve performance.

## **Recommended Steps**

### **Create custom roles**

If the built-in roles are insufficient, you can define custom roles. Here is an example of role definition for a data scientist role that can be used to prevent a user from creating creating compute resources.

```
{
    "Name": "Data Scientist Custom",
    "IsCustom": true,
    "Description": "Can run experiment but can't create or delete compute.",
    "Actions": ["*"],
    "NotActions": [
        "Microsoft.MachineLearningServices/workspaces/*/delete",
        "Microsoft.MachineLearningServices/workspaces/write",
        "Microsoft.MachineLearningServices/workspaces/computes/*/write",
        "Microsoft.MachineLearningServices/workspaces/computes/*/delete", 
        "Microsoft.Authorization/*/write"
    ],
    "AssignableScopes": [
        "/subscriptions/<subscription_id>/resourceGroups/<resource_group_name>/providers/Microsoft.MachineLearningServices/workspaces/<workspace_name>"
    ]
}
```

See the [following article](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) to learn more about how to create and assign custom roles.

### **Configure access on individual resources**

Instance level access (allowing the user to access datasetA, but not datasetB) is not yet supported in Azure ML. In instance level access, we recommend separating resources into different workspaces and use custom roles to control access.

### **Authenticate through automated workflows**

Service principal authentication can be used to authentication through automated workflows. This can be done using the Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py) as follows:

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

## **Recommended Documents**

Here is a list of additional resources which may be helpful: 

* [Set up authentication for Azure Machine Learning resources and workflows](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication)
* [Manage access to Azure Machine Learning workspace](https://docs.microsoft.com/azure/machine-learning/how-to-assign-roles)
* [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)