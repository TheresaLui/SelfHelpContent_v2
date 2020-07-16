<properties
	pageTitle="Provide general guidance and advisory"
	description="Provide general guidance and advisory"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677654"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1305df1d-4f65-4bc0-afc4-d4825784826a"
	ownershipId="AzureData_AzureDatabricks"
/>

# Provide general guidance and advisory

## **Recommended Steps**

* For guidance on setting up Databricks, look into our How-To guides here: [Azure Databricks Documentation](https://docs.microsoft.com/azure/databricks/)
* For guidance on resolving errors and setup issues go to the [Knowledge Base](https://docs.microsoft.com/azure/databricks/kb/) 
* For current status by region and to subscribe for updates on status changes, review [Azure Databricks Status Page](https://status.azuredatabricks.net/) 

### **Cluster Creation Issues**

* Error: Operation results in exceeding quota limits of Core
     * Follow [steps here](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests) to submit an expedited request for core quota limit increase
* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem.
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)

### **Jobs**
* [How to create, run and view job details](https://docs.microsoft.com/azure/databricks/jobs)

### **Connectivity**

* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
     
### **Notebook Execution Issues**

* [How to Get the Full Path to the Current Notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-path)
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username)
* [Common Errors in Notebooks](https://docs.microsoft.com/azure/databricks/kb/notebooks/common-errors-in-notebooks)
* [Cannot Run Notebook Commands After Canceling Streaming Cell](https://docs.microsoft.com/azure/databricks/kb/notebooks/streaming-notebook-stuck)



