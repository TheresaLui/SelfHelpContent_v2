<properties
  pagetitle="Virtual Network Configuration"
  service="microsoft.machinelearning"
  resource="machinelearning"
  ms.author="johwu"
  selfhelptype="Generic"
  supporttopicids="32740868"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.enterprisesecurity.virtualnetwork"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Virtual Network Configuration

A virtual network acts as a security boundary, isolating your Azure resources from the public internet. To ensure your workspace, training jobs, and inferencing jobs all remain secured behind a virtual network, take the following steps:

1. Ensure your workspace is behind a private endpoint, which requires users to connect to your workspace through private IP addresses.
2. Ensure all your associated resources (storage accounts, container registry, key vaults) are in the same virtual network as the workspace.
3. Ensure all compute and data resources are in the same virtual network as the workspace.

## **Recommended Steps**

### **Configure workspace behind a private endpoint**

To configure a new workspace behind a private endpoint:

1. Create a new machine learning workspace through the Azure Portal.
2. Click on the **Networking** tab during the creation experience.
3. Add a private endpoint by specifying the required parameters.

To configure an existing workspace behind a private endpoint:

1. Navigate to the machine learning workspace in the Azure Portal.
2. Click on the **Private endpoint connections** tab under **Settings**.
3. Add a private endpoint by specifying the required parameters.

For more detailed instructions, see the [how to configure a private link](https://docs.microsoft.com/azure/machine-learning/how-to-configure-private-link).

### **Ensure storage account is behind a virtual network**

To configure your workspace storage account behind a virtual network:

1. Navigate to the storage resource in the Azure Portal.
2. Click on the **Firewalls and virtual networks** tab under **Settings**.
3. Add your virtual network and allow trusted Microsoft services to access the resource.

For more details, see [secure Azure storage accounts with service endpoints](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#secure-azure-storage-accounts-with-service-endpoints).

### **Ensure container registry is behind a virtual network**

To configure your container registry resource to work behind a virtual network:

1. Navigate to the container registry resource in the Azure Portal.
2. Click on the **Networking** tab under **Settings**.
3. Add your virtual network to the resource.

For more details, see [enable Azure container registry ACR](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#enable-azure-container-registry-acr).

### **Ensure key vault is behind a virtual network**

To configure your key vault resource to work behind a virtual network:

1. Navigate to the key vault resource in the Azure Portal.
2. Click on the **Networking** tab under **Settings**.
3. Add your virtual network to the resource.

For details, see [secure Azure key vault](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#secure-azure-key-vault).

## **Recommended Documents**

* [Azure ML Network Security Overview](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview)
* [Azure Private Link Overview](https://docs.microsoft.com/azure/private-link/private-link-overview)
* [Azure Virtual Networks Overview](https://docs.microsoft.com/azure/virtual-network/virtual-networks-overview)
* [Azure ML Enterprise Security Overview](https://docs.microsoft.com/azure/machine-learning/concept-enterprise-security)
