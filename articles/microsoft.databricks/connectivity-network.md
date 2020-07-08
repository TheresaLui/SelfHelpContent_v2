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
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="64e0439a-9d7d-40c8-8084-9048d0306b54"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve connectivity issues with network configuration

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [A technical overview of Azure Databricks](https://azure.microsoft.com/blog/a-technical-overview-of-azure-databricks/)
* [Virtual Network Peering](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-peering.html)
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem.

