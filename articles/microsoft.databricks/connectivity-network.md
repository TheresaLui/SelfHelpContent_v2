<properties
	pageTitle="Diagnose and resolve connectivity issues with network configuration"
	description="Diagnose and resolve connectivity issues with network configuration"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677711"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="64e0439a-9d7d-40c8-8084-9048d0306b54"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues with network configuration

## **Recommended Documents**

* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [A technical overview of Azure Databricks](https://azure.microsoft.com/blog/a-technical-overview-of-azure-databricks/)
* [How to assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://kb.azuredatabricks.net/cloud/azure-vnet-single-ip.html)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem.

