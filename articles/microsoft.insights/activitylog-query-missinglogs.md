<properties 
    pageTitle="Expected information is missing from activity logs"
    description="Expected information is missing from activity logs"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="activitylog-query-missinglogs"
    productPesIds="16251"
    supportTopicIds="32684695"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- query-missinglogs -->

If you are missing log information in the response body, it is most probably due to the fact that the response body contains sensitive information which is not logged in Activity Logs. Sensitive information includes passwords, security keys, tokens etc.

If you have issues with logs missing from activity logs other than the response body, then please proceed with creating a support ticket.

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
