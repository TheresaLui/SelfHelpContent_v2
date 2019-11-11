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
/>

# Diagnose and resolve issues with connectivity to Workspace

## **Recommended Documents**

* [Workspace Permissions](https://docs.azuredatabricks.net/administration-guide/access-control/workspace-acl.html#workspace-permissions)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-inject.html)
* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem
* By default, all users can create and modify workspace objects. However, if administrator enables workspace access control, individual permissions determine a user’s abilities. Workspace Access Control is only available in the Premium SKU. Enabling Workspace Access Control will allow users to control who can view, edit, and run notebooks in their workspace. 
If you have this enabled, please give the required permissions as needed: [Workspace Permissions](https://docs.azuredatabricks.net/administration-guide/admin-settings/workspace-acl.html#workspace-permissions)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* [Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
