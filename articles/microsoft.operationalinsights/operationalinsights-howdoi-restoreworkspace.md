
<properties
pageTitle="Restore deleted workspace"
description="Restore deleted workspace"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="777445d0-915a-43d5-adfc-749a17c03410"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612520"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Restore deleted workspace
The restore operation is available up to 14 days from deletion time and it’s unrecoverable afterwards. It recovers the workspace to its state at the time of deletion, but not all dependent resources such as solutions, linked automation account or data sources can be fully recovered, unrecovered resources need to be reconfigured after the workspace recovery. Since data ingestion stops on workspace deletion, the oldest data after workspace recovery is of the workspace deletion time.

## **Recommended Steps**
* You need Contributor permissions to the subscription and resource group where the workspace was associated before the soft-delete operation
* Recover the workspace by re-creating it using any of the workspace create methods: [Azure portal](https://portal.azure.com/#create/hub), [PowerShell](https://docs.microsoft.com/powershell/module/az.operationalinsights/New-AzOperationalInsightsWorkspace?view=azps-3.5.0) or [REST API](https://docs.microsoft.com/rest/api/loganalytics/workspaces/createorupdate) with the deleted workspace details:<br>
  * Subscription ID
  * Resource Group name
  * Workspace name
  * Region<br>


## **Recommended Documents**

* [Recover workspace](https://docs.microsoft.com/azure/azure-monitor/platform/delete-workspace#recover-workspace)
* [Collect agent data sources](https://docs.microsoft.com/azure/azure-monitor/platform/agent-data-sources)
* [Collect Azure service logs and metrics for use in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/collect-azure-metrics-logs)
* [Data collection details for management solutions](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-inventory)
* [Adding Azure Automation resources to a management solution](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-resources-automation)<br>
