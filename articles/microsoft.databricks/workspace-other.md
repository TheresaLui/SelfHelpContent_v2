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

## **Recommended Steps**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* If you are unable to launch or access Azure Databricks workspace due to error "User does not have Contributor or Owner role", the issue is by design. Enable access to users by modifying IAM roles and assign **Contributor** or **Owner** role following steps [here](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--assign-account-admins). User should be added **individually** as adding AD group is *not supported* yet.

* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* [Managed Applications and Locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks)

* Deployment of workspace through ARM Templates fails if you use existing resource group name as a managed resource group. Always ensure [Managed Resource group](https://docs.microsoft.com/azure/managed-applications/overview#managed-resource-group) in ARM template doesn't already exist within the subscription.

* Please avoid having any special characters (- or _) as the first or last character in workspace name. Maximum length for Managed resource group Name: 90 characters. Workspace creation will fail due to invalid characters. 

* [Error: Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch#instances-unreachable)
* [Retrieve the current username for the notebook](https://docs.microsoft.com/azure/databricks/kb/notebooks/get-notebook-username). This is currently supported for:

	* Standard clusters in both Scala and Python
	* High Concurrency clusters in Python with Credential Passthrough **disabled**
