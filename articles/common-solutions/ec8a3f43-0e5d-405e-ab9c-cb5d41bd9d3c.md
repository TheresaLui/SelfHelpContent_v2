<properties
  pagetitle="Create or delete workspace&#xD;"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="yossiy,neghuman,shemers"
  selfhelptype="Generic"
  supporttopicids="32782939"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="ec8a3f43-0e5d-405e-ab9c-cb5d41bd9d3c"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Create or delete workspace

## **Recommended Steps** 

### **Delete a Log Analytics workspace**

There are two different ways to delete a Log Analytics workspace:

* [Soft delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#soft-delete-behavior): this is the default delete method that allows the recovery of the workspace, including its data and connected agents, within 14 days. After the soft-delete period, the workspace and its data are permanently purged and nonrecoverable, and the workspace name is released, which means that you can use it to create a new workspace.
* [Permanent delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete): this action purges the workspace, its data, and releases the workspace name immediately, which means that you can create a new workspace using the same name. For simplicity, you can also execute it in [Azure REST API Reference](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete#code-try-0) site by adding the parameter `force` with the value `true`.<br>

Keep the following points in mind:

* You must have Log Analytics Contributor permissions to delete a Log Analytics workspace
* You can delete a workspace using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace?view=azurermps-6.13.0#examples), [REST API](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete), or in the [Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#azure-portal)
* When you delete a workspace, installed solutions and linked services such as Azure Automation account are permanently removed and can’t be recovered<br>

### **Create a Log Analytics workspace**

* You must have Log Analytics Contributor permissions to create a Log Analytics workspace
* You can create a Log Analytics workspace in any of the supported [regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)
* If you get the error message "This workspace name is already in use" when creating a workspace, it could be due to one of the following reasons:
	
	* The workspace name isn't available and is being used
	* The workspace was deleted during the last 14 days and its name reserved for the soft-delete period. To override the soft-delete period and immediately delete the workspace and create a new workspace with the same name, do the following:

      1. [Recover](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace) your workspace
      2. [Permanently delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete) your workspace
      3. Create a new workspace using the deleted workspace name
 
## **Recommended Documents**

* [Soft-delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#soft-delete-behavior)
* [Permanent delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)
* [Recover a workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Log Analytics supported regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)<br>
