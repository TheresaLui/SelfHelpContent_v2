<properties 
    pageTitle="I cannot find logs for an expected event"
    description="I cannot find logs for an expected event"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="activitylog-missing-logs"
    productPesIds="16251"
    supportTopicIds="32684695"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- missing-logs -->
Activity logs retains the logs for 90 days, users can choose to store the logs in Azure storage (via diagnostic settings) if you would like to retain logs longer than the stipulated period. Following recommendations further provide checks and reference to ensure you are able to retrieve logs as expected. Please proceed to create a support ticket if your problem falls outside of the scope mentioned here.

## **Recommended Steps**

1. Refer to the [diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings) to ensure it's correct setup and then setting up the destination
1. Refer to the [supported categories](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-schema#next-steps) of logs supported by Activity logs
1. Ensure that the logs you would want to view are not older than 90 days

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
