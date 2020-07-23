<properties
	pageTitle="Diagnose and resolve issues with Workspace launch failure in VNET injected workspace"
	description="Diagnose and resolve issues with Workspace launch failure in VNET injected workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677735, 32688714"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e900d305-69fb-4a05-a0ce-68e94b4dbce2"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Workspace launch failure in VNET injected workspace

## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Steps to Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://kb.azuredatabricks.net/cloud/azure-vnet-single-ip.html)
* If you are unable to launch or access Azure Databricks workspace due to error "User does not have Contributor or Owner role", the issue is by design. Enable access to users by modifying IAM roles and assign **Contributor** or **Owner** role following steps [here](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--assign-account-admins). User should be added **individually** as adding AD group is *not supported* yet.
