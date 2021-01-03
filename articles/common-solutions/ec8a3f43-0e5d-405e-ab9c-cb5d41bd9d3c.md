<properties
  pagetitle="Create workspace&#xD;"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="neghuman,shemers,yossiy"
  selfhelptype="Generic"
  supporttopicids="32782939"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="ec8a3f43-0e5d-405e-ab9c-cb5d41bd9d3c"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Create workspace

## **Recommended Steps** 

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