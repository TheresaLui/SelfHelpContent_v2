<properties
  pagetitle="Problem provisioning or managing workspace"
  service="microsoft.machinelearning.workspace"
  resource="machinelearning"
  ms.author="roastala,johwu"
  selfhelptype="Generic"
  supporttopicids="32690836"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.workspace.manage"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Problem provisioning or managing workspace

## **Recommended Steps**

### **Don't have permission to create the workspace**

If you receive a permission failure when creating a workspace:

1. Make sure your role has `Microsoft.MachineLearningServices/workspaces/write` permission.
2. If this is the first time you are creating a workpsace, also make sure your role has `Microsoft.MachineLearningServices/register/action` permission.

### **Can't select or update to Enterprise SKU**

The enterprise SKU for Azure ML has been deprecated. All features will be offered in the basic workspace SKU.

### **Problem with associated resources**

New associated resources (storage account, key vault, container registry, application insights) are always provisioned with each workspace. The container registry is only provisioned after you submit your first run.

- If you wish to use existing associated resources, you can specify the parameters during workspace creation.
- If your workspace has a private endpoint, make sure all the associated resources are inside the same virtual network as the workspace.
- There is currently no support for replacing the associated resources after the workspace has been created.

### **Problem setting up workspace with private endpoint**

If you are having issues with your private link workspace:

1. Ensure all your associated resources (storage accounts, container registry, key vaults) are in the same virtual network as the workspace.
2. Ensure all compute and data resources are in the same virtual network as the workspace.
3. Ensure you have private DNS zone quota by submitting a support request under the **Private Endpoint and Private DNS zone allowance request** problem subtype.

## **Recommended Documents**

* [How to create a workspace](https://docs.microsoft.com/azure/machine-learning/how-to-manage-workspace?WT.mc_id=Portal-Microsoft_Azure_Support&tabs=azure-portal)
* [Network security overview](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview)
* [Data security overview](https://docs.microsoft.com/azure/machine-learning/how-to-high-availability-machine-learning)
* [Role-based access control overview](https://docs.microsoft.com/azure/machine-learning/how-to-assign-roles)
