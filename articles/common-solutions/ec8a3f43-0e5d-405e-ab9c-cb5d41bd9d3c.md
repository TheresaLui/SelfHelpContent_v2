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

Most customers can successfully create a Log Analytics workspace using the following steps.

## **Recommended Steps** 

* Make sure that you have Log Analytics Contributor permissions
* Create the Log Analytics workspace in a supported [region](https://azure.microsoft.com/global-infrastructure/services/?products=monitor&regions=all)
* When creating the workspace, if you get the error "This workspace name is already in use," the cause may be one of the following reasons:
	* The workspace name is already in use (that is, it isn't available)
	* The workspace was deleted in the last 14 days and its name is reserved for the soft-delete period. To override the soft-delete period, delete the workspace, and create a new workspace with the same name, do the following:

      1. [Recover the workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
      2. [Permanently delete the workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#permanent-workspace-delete)
      3. Create a new workspace using the deleted workspace name
 
## **Recommended Documents**

* [Soft-delete behavior](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#soft-delete-behavior)
* [Manage access to log data and workspaces in Azure Monitor](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access?toc=/azure/azure-monitor/toc.json#managing-access-to-log-analytics-using-azure-permissions)
