
<properties
pageTitle="Create or delete workspace"
description="Create or delete workspace"
service="microsoft.operationalinsights"
articleTags="tag"
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

## Create or delete workspace

### **Delete Log Analytics workspace**

When you delete a Log Analytics workspace, a soft-delete operation is performed to allow the recovery of the workspace including its data and connected agents within 14 days. Then, the workspace and its data are permanently purged and are non-recoverable - The workspace name is 'released' and you can use it to create a new workspace. 

* You can delete a workspace using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace?view=azurermps-6.13.0), [REST API](https://docs.microsoft.com/rest/api/loganalytics/workspaces/delete), or in the [Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#azure-portal)
* Installed solutions and linked services such as Azure Automation account are permanently removed from the workspace and can’t be recovered
* You can **override the soft-delete behavior** and [delete your workspace permanently](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)

### **Creating Log Analytics workspace**

* You must have *'Log Analytics Contributor'* permissions to create Log Analytics workspace
* You can create Log Analytics workspace in any of the supported [regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)
 
## **Recommended Documents**

* [Permanent workspace delete](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)
* [Recover a workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
* [Log Analytics supported regions](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)<br>
