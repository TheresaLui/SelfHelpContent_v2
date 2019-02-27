
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
cloudEnvironments="Public, Fairfax"
/>

# Restore deleted workspace
Log Analytics workspace is often used as central store for data coming from multiple sources and accidental delete could be impactful. The restore operation is available up to 14 days from delete time and it’s unrecoverable afterwards. it recovers the workspace to its state at the time of deletion, but not all dependent resources such as solutions, linked automation account or data sources can be fully recovered, unrecovered resources need to be reconfigured after the workspace recovery. Data ingestion stops when workspace is deleted and this data is unrecoverable. After the workspace recovery, the last data will be of the time of workspace deletion.

## **Recommended Steps**
1. Recovery is performed via support case only – submit a new support request for Log Analytics workspace recovery.
1. Provide the workspace name and workspace Id<br>

## **Recommended Documents**
* [Collect agent data sources](https://docs.microsoft.com/azure/azure-monitor/platform/agent-data-sources)
* [Collect Azure service logs and metrics for use in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/collect-azure-metrics-logs)
* [Data collection details for management solutions](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-inventory)
* [Adding Azure Automation resources to a management solution](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-resources-automation)<br>