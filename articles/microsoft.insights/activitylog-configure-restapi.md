<properties 
    pageTitle="Configuring activity log and exporting using REST API"
    description="Configuring activity log and exporting using REST API"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="activitylog-configure-restapi"
    productPesIds="16251"
    supportTopicIds="32684694"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- configuring-restapi -->

The activity log contains all write operations (PUT, POST, DELETE) for your resources. It doesn't include read operations (GET). You can use the activity logs to find an error when troubleshooting or to monitor how a user in your organization modified a resource.
You can retrieve information from activity logs and export them by creating diagnostic logs settings via REST API


## **Recommended Steps**

1. The REST operations for working with the activity log are part of the [Insights REST API](https://docs.microsoft.com/rest/api/monitor/). To retrieve activity log events, see [List the management events in a subscription](https://docs.microsoft.com/rest/api/monitor/activitylogs).
1. Review [how to view activity logs to monitor actions on resources](https://docs.microsoft.com/azure/azure-resource-manager/management/view-activity-logs#rest-api)
1. Review overview of [diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings)
1. Refer to how to create [diagnostic settings via REST API](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-rest-api)

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
