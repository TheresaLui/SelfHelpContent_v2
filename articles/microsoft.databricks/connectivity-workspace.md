<properties
	pageTitle="Diagnose and resolve issues with connectivity to workspace"
	description="Diagnose and resolve issues with connectivity to Workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677673"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="b0d6610b-0a52-4891-a974-0fdd2f4ce176"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with connectivity to Workspace

## **Recommended Documents**

### **Configuration and Setup**

* [Workspace Access Control](https://docs.microsoft.com/azure/databricks/administration-guide/access-control/workspace-acl)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem

### **Troubleshooting Errors**

* [How to resolve error: Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
