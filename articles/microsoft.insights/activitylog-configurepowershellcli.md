<properties 
    pageTitle="Configuring activity log and exporting using Powershell or CLI"
    description="Configuring activity log and exporting using Powershell or CLI"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="activitylog-configure-powershellcli"
    productPesIds="16251"
    supportTopicIds="32684689"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- configuring-configure-powershellcli -->
The activity log contains all write operations (PUT, POST, DELETE) for your resources. It doesn't include read operations (GET). You can use the activity logs to find an error when troubleshooting or to monitor how a user in your organization modified a resource.
You can retrieve information from activity logs and export them by creating diagnostic logs settings via Powershell or Azure CLI. 

## **Recommended Steps**

1. To retrieve information from activity logs via Powershell, [follow these instructions](https://docs.microsoft.com/azure/azure-resource-manager/management/view-activity-logs#powershell)
1. To retrieve information from activity logs via Azure CLI, [follow these instructions](https://docs.microsoft.com/azure/azure-resource-manager/management/view-activity-logs#azure-cli)
1. Review [overview of diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings)
1. Refer to [how to create diagnostic settings using powershell](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-diagnostic-settings-using-powershell)
1. For Azure CLI, [Create diagnostic setting in Azure Monitor using a Resource Manager template](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-template#activity-log) to create a Resource Manager template and deploy it with CLI. Refer to the example of a CLI command to create a diagnostic setting [here](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-diagnostic-settings-using-azure-cli)

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
