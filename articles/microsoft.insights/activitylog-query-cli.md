<properties 
    pageTitle="Querying activity logs using Azure CLI"
    description="Querying activity logs using Azure CLI"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="activitylog-query-cli"
    productPesIds="16251"
    supportTopicIds="32684692"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- configuring-query-cli -->

The activity log contains all write operations (PUT, POST, DELETE) for your resources. It doesn't include read operations (GET). You can use the activity logs to find an error when troubleshooting or to monitor how a user in your organization modified a resource.
Follow the recommended steps if you are experiencing an issue with using querying activity logs using Azure CLI.


## **Recommended Steps**

1. Refer to [how to retrieve activity logs using Azure CLI](https://docs.microsoft.com/azure/azure-resource-manager/management/view-activity-logs#azure-cli) 
1. Evaluate you have the [permissions to query the activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles)

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)