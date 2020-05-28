<properties
	pageTitle="Diagnose and resolve issues with Workspace"
	description="Diagnose and resolve issues with Workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677733"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="32507757-3fe2-45eb-9f0f-fd046dd47472"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Workspace

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://kb.azuredatabricks.net/cloud/azure-vnet-single-ip.html)
* [Managed Applications and Locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks)
* Deployment of workspace through ARM Templates fails if you use existing resource group name as a managed resource group. Always ensure [Managed Resource group](https://docs.microsoft.com/azure/managed-applications/overview#managed-resource-group) in ARM template doesn't already exist within the subscription.
* It is not possible to deploy two workspaces with same managed resource group name. If you try to create second workspace with the same managed resource group, it will fail also puts first workspace inconsistent state.
* While deploying workspace through ARM Template, you can’t have Managed Resource Group Name as Existing Resource Group where workspace is present
* Please avoid having any special characters (- or _) as the first or last character in workspace name. Maximum length for Managed resource group Name: 90 characters. Workspace creation will fail due to invalid characters. 
