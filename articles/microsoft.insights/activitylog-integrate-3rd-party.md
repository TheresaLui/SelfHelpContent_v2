<properties 
    pageTitle="Integrating activity log with 3rd party SIEM tools"
    description="Recommendations for integrating activity log with 3rd party SIEM tools"
    service="microsoft.insights"
    resource=""
    authors="vgorbenko"
    ms.author="vitalyg"
    selfHelpType="generic"
    articleId="activitylog-integrate-3rd-party"
    productPesIds="16251"
    supportTopicIds="32688872"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- activitylog-integrate-3rd-party -->
For best performance and reliability, we recommend configuring export of the Activity Log events to the **Event Hub** by using [Subscription Diagnostic Settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription). Many SIEM partners have existing integrations with Event Hub. You can see some of the 3rd party tools and partners listed at [Partner tools with Azure Monitor integration](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs#partner-tools-with-azure-monitor-integration).

## **Recommended Steps**

* Configure export of the Activity Log events to the Event Hub by using [Subscription Diagnostic Settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* Follow the guidance from your SIEM tool provider for integrating with Event Hub

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
