
<properties
pageTitle="Create or delete workspace"
description="Create or delete workspace"
service="microsoft.operationalinsights"
resource="workspaces"
ownershipId="AzureMonitoring_LogAnalytics"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder="11"
selfHelpType="resource"
supportTopicIds="32612513"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, Mooncake"
	articleId="a5b6bf14-b4ea-40b5-bac8-286416838545"
/>

# Create or delete workspace

### **Delete Log Analytics workspace**

When you delete a Log Analytics workspace, a soft-delete operation is performed by default to allow the recovery of the workspace including its data and connected agents within 14 days. After the soft-delete period, the workspace and its data are permanently purged and are non-recoverable, the workspace name is 'released' and you can use it to create a new workspace. 

* You must have *'Log Analytics Contributor'* permissions to delete a Log Analytics workspace
* You can delete a workspace using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace?view=azurermps-6.13.0#examples), [REST API](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete), or in the [Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#azure-portal)
* Installed solutions and linked services such as Azure Automation account are permanently removed from the workspace and can’t be recovered
* If your workspace was deleted during the last 14 days, hence in soft-delete state and you want to create a new workspace with the same name - you need to:<br>
  1. [Recover](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace) your workspace
  2. Permanently delete the workspace by [overriding the soft-delete behavior](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete) using this REST API
		```rst
		DELETE https://management.azure.com/subscriptions/<subscription-id>/resourcegroups/<resource-group-name>/providers/Microsoft.OperationalInsights/workspaces/<workspace-name>?api-version=2015-11-01-preview&force=true
		```
	3. Create a new workspace using the deleted workspace name<br>

### **Creating Log Analytics workspace**

* You must have *'Log Analytics Contributor'* permissions to create Log Analytics workspace
* You can create Log Analytics workspace in any of the supported [regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all) 
* If you get an error message '*This workspace name is already in use*' when creating a workspace, it could be due to:<br>
	* Workspace name isn't available and being used
	* Workspace was deleted during the last 14 days and its name is reserved for the soft-delete period - In this case follow steps 1 to 3 above<br>

 
## **Recommended Documents**

* [Permanent workspace delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)
* [Recover a workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Log Analytics supported regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)<br>
