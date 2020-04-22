<properties 
    pageTitle="My activity logs are not showing up when expected"
    description="The activity logs entries are not showing up or delayed"
    service="microsoft.insights"
    resource=""
    authors="vgorbenko"
    ms.author="vitalyg"
    selfHelpType="generic"
    articleId="activitylog-delayed"
    productPesIds="16251"
    supportTopicIds="32684696"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- activitylog-delayed -->

Most Activity Log entries are expected to show up in the Azure Portal within 15 minutes after the event has occurred. The **Service Health**, **Resource Health**, and **Security** events may take extra time, as they often require automated analysis or manual intervention before being submitted to the log. In any case, the *eventTimestamp* property of the event is backdated to the time when the incident has happened, while the *submissionTimestamp* property tracks the time when the Activity Log received the log entry.

## **Recommended Steps**

* Check again in 15 minutes to see if the Activity Log starts showing the expected events. You may need to wait longer if you are looking for the Service Health, Resource Health, or Security events
* Use the *eventTimestamp* property to identify when the incident has occurred

## **Recommended Documents**

* [Overview of Azure activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity log with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
