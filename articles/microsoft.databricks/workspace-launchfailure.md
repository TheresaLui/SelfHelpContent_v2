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

## **Recommended Steps**

* When signing in to the Azure Databricks workspace, you may encounter the following error: 
  
  ```
  We’ve encountered an error logging you in. Databricks support has been alerted and will begin looking into the issue right away. 
  ```
  To work around this problem, open a new tab in Google Chrome, or close the browser and erase its history.
If this does not resolve your issue, understand that we have ongoing maintenance or outages to resolve these kinds of errors. Check the [Databricks status page](https://status.azuredatabricks.net/).

* If you are unable to launch or access the Azure Databricks workspace due to error "User does not have Contributor or Owner role", the issue is by design. Enable access to users by modifying IAM roles and assign **Contributor** or **Owner** role. Make sure to add each user individually, as adding an AD group is not supported. [See the full instructions](https://docs.microsoft.com/azure/databricks/administration-guide/account-settings/account#--assign-account-admins). 
  
## **Recommended Documents**

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes
* [Steps to Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Instances unreachable](https://docs.microsoft.com/azure/databricks/kb/clusters/cluster-failed-launch)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)
* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations.
