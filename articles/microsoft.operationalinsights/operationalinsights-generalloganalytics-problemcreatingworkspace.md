<properties
  pagetitle="Delete workspace&#xD;"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="neghuman,yossiy"
  selfhelptype="Generic"
  supporttopicids="32612513"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="a5b6bf14-b4ea-40b5-bac8-286416838545"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Delete workspace

## **Recommended Steps** 

### **Delete Log Analytics workspace**

There are two different ways to delete a Log Analytics workspace:

* [Soft-delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#soft-delete-behavior): This default delete method allows the recovery of the workspace including its data and connected agents within 14 days. After the soft-delete period, the workspace and its data are permanently purged and are not recoverable, the workspace name is released, and you can use it to create a new workspace.
* [Permanent-delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete): This method purges the workspace and its data, and releases the workspace name immediately. This lets you create a new workspace using the same name. For simplicity, you can also execute it in [Azure REST API Reference](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete#code-try-0) site when adding this parameter: `force` with this value: `true`.<br>

**Important:** Keep the following in mind:

* You must have **Log Analytics Contributor** permissions to delete a Log Analytics workspace
* You can delete a workspace using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace?view=azurermps-6.13.0#examples), [REST API](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete), or in the [Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#azure-portal)
* When you delete a workspace, installed solutions and linked services, such as an Azure Automation account, are permanently removed and can’t be recovered<br>
 
## **Recommended Documents**

* [Soft-delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#soft-delete-behavior)
* [Permanent-delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)
* [Recover a workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Log Analytics supported regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)<br>
