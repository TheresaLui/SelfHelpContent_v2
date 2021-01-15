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

* Review [Azure Databricks Status Page](https://status.azuredatabricks.net/) for current status by region and to subscribe for updates on status changes

* Use the following steps to resolve the error, "<subscription id> does not have authorization to perform action Microsoft.Resources/subscriptions/resourcegroups/delete over scope":
	
     * Log in to Azure portal and navigate to the Databricks Workspace that needs to be deleted
     * Select **Managed Resource Group** 
     * If there are no [locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks), select **Delete**
     * After the Managed Resource group is deleted, proceed with deleting the workspace
     
* The cleanup of the workspace is an asynchronous process. It takes about 5-10 minutes to clean up cluster resources such as VNet, virtual machines, storage, and NSG.  If you just initiated it, wait and then check after 5-10 minutes.

* [How to discover who deleted a workspace in Azure portal](https://docs.microsoft.com/azure/databricks/kb/administration/who-deleted-workspace)
