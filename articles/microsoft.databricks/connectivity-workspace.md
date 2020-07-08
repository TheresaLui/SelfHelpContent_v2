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
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b0d6610b-0a52-4891-a974-0fdd2f4ce176"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with connectivity to Workspace

## **Recommended Documents**

Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

### **Configuration and Setup**

* [Workspace Access Control](https://docs.microsoft.com/azure/databricks/administration-guide/access-control/workspace-acl)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* [Virtual Network Peering](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-peering)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network#--step-3-create-user-defined-routes-and-associate-them-with-your-azure-databricks-virtual-network-subnets) to solve this problem
* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* You can get the public/private IP address of your [driver or executor node(s)](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#--sparknode) by running this command in a notebook:

```
	%sh
	curl -H Metadata:true "http://169.254.169.254/metadata/instance/network?api-version=2017-08-01"
```

### **Troubleshooting Errors**

* [How to resolve error: Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
