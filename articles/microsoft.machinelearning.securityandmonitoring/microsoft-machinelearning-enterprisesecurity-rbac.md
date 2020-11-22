<properties
  pagetitle="Setting up role-based access control (RBAC)"
  service="microsoft.machinelearning"
  resource="machinelearning"
  ms.author="johwu"
  selfhelptype="Generic"
  supporttopicids="<TO_UPDATE>"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.enterprisesecurity.rbac"
  ownershipid="AzureML_AzureMachineLearningServices" />

# Setting up role-based access control (RBAC)

An Azure Machine Learning workspace is an Azure resource. Like other Azure resources, when a new Azure Machine Learning workspace is created, it comes with three default roles which can be assigned to users.

1. **Reader**: Read-only actions in the workspace. Readers can list and view assets in a workspace, but can't create or update these assets.
2. **Contributor**: View, create, edit, or delete (where applicable) assets in a workspace. For example, contributors can create an experiment, create or attach a compute cluster, submit a run, and deploy a web service.
3. **Owner**: Full access to the workspace, including the ability to view, create, edit, or delete (where applicable) assets in a workspace. Additionally, you can change role assignments.

When changing role assignments, it may take up to 30 minutes for them to take effect, as application caches are used to improve performance.

## **Recommended Steps**

### **Create custom roles**

If the built-in roles are insufficient, you can define custom roles. Here is an example of role definition for a data scientist role which can be used to prevent a user from creating creating compute resources.

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

Instance level access (ie, allow user to access datasetA but not datasetB) are not yet supported in Azure ML. If instance level access, it is recommended to separate resources into different workspaces and use custom roles to control access.

## **Recommended Documents**

Here is a list of additional resources which may be helpful: 

* [Manage access to Azure Machine Learning workspace](https://docs.microsoft.com/azure/machine-learning/how-to-assign-roles)
* [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)