<properties
    pageTitle="Issues with managing Training clusters or Compute Instance"
    description="Article on issues with Managing Amlcompute and Compute Instance"
    service="microsoft.machinelearning"
    resource="Microsoft.MachineLearningServices/workspaces/computes"
    authors="nishankgu"
    ms.author="nigup"
    selfHelpType="generic"
    articleId="microsoft-machinelearning-amlcompute-manage.md"
    supportTopicIds="32690861"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# When you are hitting issues creating compute such as a Training Cluster, Compute Instance or an AKS cluster

## **Recommended Steps**

### If you're experiencing quota issues:
1. A quota is a limit that is enforced by Azure to prevent fraudulent subscriptions from using Azure capacity, and to control capacity overruns in a particular region. If you are creating a training cluster or a compute instance, they share the same quota, and the quota is internal to the Azure Machine Learning compute. Check if you have enough quota by going to the **Quotas + Usages** section in your workspace for the region that you're experiencing this issue in.
2. It's also possible that your subscription owner has applied quota limits at your workspace level to better distribute capacity across various workspaces in your subscription. You may need to contact them to request an increase in the quota.
3. If you have sufficient quota, it's possible that another cluster or instance in your workspace is using the quota. Because quota is at a VM series level, and clusters or instances are specific to a VMSize, it's possible that another cluster/instance is sharing and using quota.

### If you're consistently experiencing an issue at creation time:
1. Your region could be **out of capacity**, which is generally represented in the error message at the time of allocation failure. You can try using a different VM family, or retry at a later time.
2. You could also be using an **unsupported VMsize** in the region of your workspace. We document the supported VM sizes and generally keep the list up to date with the latest SKUs supported by Azure.
3. It's also possible that your **VNet configuration** on your compute target could be misconfigured and preventing Azure services from reaching them, leading to situations such as unusable nodes. Managed Compute has a very specific VNet configuration setup, as detailed in our documentation.
4. If compute instance is created behind VNET, make sure you have an **NSG rule** where inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning. Inbound TCP traffic on ports 29876 and 29877 from a Service Tag of BatchNodeManagement also needs to be allowed through NSG. If you are behind a proxy ensure that web socket communication is not disabled for azureml.net and azureml.ms domains. If workspace storage account is attached to a virtual network please ensure compute instance is also deployed to same virtual network/subnet. If you are using custom DNS please check you settings. For details, see [documentation for virtual network setup](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet#compute-instance).
5. If you've created a compute instance in a **private link workspace**, make sure that you're accessing the compute instance from within virtual network. If you are using custom DNS or a host file, make sure that you have an entry for `<instance-name>.<region>.instances.azureml.ms` with the private IP address of the workspace private endpoint. If you are using custom DNS you might need to setup a DNS forwarder. You also need to setup a private endpoint to Azure file share if workspace storage is using private link. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-portal).
6. Configure firewall and user-defined routes according to [these instructions](https://docs.microsoft.com/azure/machine-learning/how-to-access-azureml-behind-firewall).
7. Currently, creating on behalf of compute instance does not support SSH.
8. Only the creator of compute instance is able to run notebooks on the compute instance. However, there is a "create on behalf of" feature in preview that allows administrators to create and assign a compute instance to another user to run notebooks.
9. For compute instance, do not delete the `azureml_py36` conda environment or the Python 3.6 - AzureML kernel. These are needed for Jupyter/JupyterLab functionality.
10. If you need to download temporary data to compute instance, use the temporary disk (/mnt).
11. Currently, auto-shutdown on compute instance is not supported.
12. For creating a compute instance the following RBAC permissions are needed:-
* *Microsoft.MachineLearningServices/workspaces/computes/write*
* *Microsoft.MachineLearningServices/workspaces/checkComputeNameAvailability/action*
13. **Important:** Compute instance is a managed, hosted on behalf of offering in which underlying resources will no be deployed in customer Azure subscription. Only network security group, public IP address, and load balancer are deployed in customer subscription. If you have a policy blocking public IP, then compute instance deployment will fail. We have a no public IP compute instance feature in private preview.

## **Recommended Documents**

* [Learn how to view your Azure Machine Learning quota](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#view-your-usage-and-quotas)
* [Learn more about Managed Compute Clusters and Instances](https://docs.microsoft.com/azure/machine-learning/concept-compute-target)
* [Understand our recommended VNet setup](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet#compute-instance)
* [View Azure Supported VM sizes by Region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines)
* [Configure private links](https://docs.microsoft.com/azure/machine-learning/how-to-configure-private-link?tabs=python)
