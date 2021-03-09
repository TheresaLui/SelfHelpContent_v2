<properties
	pageTitle="Diagnose and resolve issues with Workspace delete"
	description="Diagnose and resolve issues with Workspace delete"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677734"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="178b9906-c5b3-4eed-9a7a-dac993391ade"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Workspace deletion

## **Recommended Steps**

* Review the [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes.

* Use the following steps to delete Azure Databricks workspace:
	
     * Log in to Azure portal as the workspace owner (the user who created the workspace) and navigate to the Databricks Workspace that needs to be deleted
     * Select **Azure Delete** and then **OK**. The cleanup of the workspace is an asynchronous process. It takes about 5-10 minutes to clean up cluster resources such as VNet, virtual machines, storage, and NSG.  If you just initiated it, wait and then check after 5-10 minutes.
  
  It is important to note that Managed Resource Group will be deleted automatically after the workspace is deleted. Managed Resource Group is locked by design, so trying to delete it first would cause errors. Make sure to delete workspace itself first.
  
  ## **Recommended Documents**
     
* [How to discover who deleted a workspace in Azure portal?](https://docs.microsoft.com/azure/databricks/kb/administration/who-deleted-workspace)
