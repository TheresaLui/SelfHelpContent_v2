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
	cloudEnvironments="public"
	articleId="32507757-3fe2-45eb-9f0f-fd046dd47472"
/>

# Diagnose and resolve issues with Workspace

## **Recommended Documents**

* [Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://kb.azuredatabricks.net/cloud/azure-vnet-single-ip.html)
* Deployment of workspace through ARM Templates fails, If you use existing resource group name as a managed resource group. Always ensure [Managed Resource group](https://docs.microsoft.com/en-us/azure/managed-applications/overview#managed-resource-group) in ARM template  doesn't exist within subscription.
* It is not possible to deploy two workspaces with same managed resource group name. If you try to create second workspace with the same managed resource group, it will fail also puts first workspace inconsistent state.
* While deploying workspace though ARM Template, You can’t have Managed Resource Group Name as Existing Resource Group where workspace is present.
* Please avoid having any special characters (- or _) as the first or last character in workspace name. Maximum length for Managed resource group Name: 90 characters. Otherwise workspace creation fails due to invalid characters. 
