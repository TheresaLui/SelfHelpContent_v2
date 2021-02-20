<properties
  pagetitle="&lt;-- can't-view-ActivityLog-LogAnalytics --&gt;&#xD;"
  service="microsoft.insights"
  resource=""
  ms.author="shemers"
  selfhelptype="Generic"
  supporttopicids="32745408,32684685"
  resourcetags=""
  productpesids="16251,15725"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake,blackforest"
  articleid="activitylog-cannotviewlog-loganalytics"
  ownershipid="AzureMonitoring_AzureMetrics" />
# <-- can't-view-ActivityLog-LogAnalytics -->

Activity logs retain the logs for 90 days. You can choose to store the logs in Azure storage (via diagnostic settings) if you want to retain logs longer than 90 days. Be sure to follow recommendations for checks and references to ensure that you can retrieve logs as expected. If your issue falls out of the scope mentioned here, create a support ticket. 

## **Recommended Steps**

1. If you are using [legacy methods](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log#legacy-collection-methods) to export an activity log, consider using diagnostic settings. 
1. Refer to the [diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings) to ensure you have the correct setup for exporting the activity log to Log Analytics. Learn more about [exporting activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log#send-to-log-analytics-workspace).
1. Refer to the [supported categories](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-schema#next-steps) of logs supported by activity logs
1. If not stored already, ensure that the logs you want to view are not older than 90 days

## **Recommended Documents**

* [Overview of Azure activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)
* [Collect Azure activity logs with diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings-subscription)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
* [Alerts on activity logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
