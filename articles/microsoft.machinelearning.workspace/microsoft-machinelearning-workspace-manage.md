<properties
  pagetitle="Managing associated resources (storage, key vault, container registry, app insights)&#xD;"
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
# Managing associated resources (storage, key vault, container registry, app insights)

All workspaces consist of a set of associated resources (storage account, key vault, container registry, application insights). During workspace provisioning, you can choose either to create them as new resources or tp select existing resources.

## **Recommended Steps**

### **Problem with storage account**

If you have issues with the associated storage account, check the following settings:

- Hierarchical namespaces are not enabled on the storage account. Hierarchical namespaces are not yet supported in Azure ML.
- The storage is not a premium account. Premium accounts are not yet supported in Azure ML.
- If your workspace is behind a private endpoint, make sure your storage is also behind the same virtual network.

### **Problem with key vault**

If you have issues with the associated key vault, check the following settings:

- If you regenerated the keys to your datastores, make sure to also update this in the workspace key vault. See the [documentation](https://docs.microsoft.com/azure/machine-learning/how-to-change-storage-access-key) for instructions.
- If your workspace is behind a private endpoint, make sure your key vault is also behind the same virtual network.

### **Problem with container registry**

If you have issues with the associated container registry, check the following settings:

- If your workspace has no associated container registry, this means that you haven't registered any images yet. Container registries are provisioned only after you submit your first run, when the first image is built. If you want to have a container registry from the beginning, select this option during workspace provisioning.
- If your workspace is behind a private endpoint, make sure your container registry is also behind the same virtual network.
- If your workspace is behind a private endpoint, ensure you have private DNS zone quota by submitting a support request under the **Private Endpoint and Private DNS zone allowance request** problem subtype.

### **Problem with application insights**

If you have issues with the associated application insights, check the following settings:
- If you want to adjust data retention period and details, see the [documentation](https://docs.microsoft.com/azure/azure-monitor/app/data-retention-privacy#how-long-is-the-data-kept)

## **Recommended Documents**

* [How to create a workspace](https://docs.microsoft.com/azure/machine-learning/how-to-manage-workspace?WT.mc_id=Portal-Microsoft_Azure_Support&tabs=azure-portal)
* [Workspace overview](https://docs.microsoft.com/azure/machine-learning/concept-workspace)
