<properties
    pageTitle="An activity log alert fired when it shouldn't have"
    description="An activity log alert fired when it shouldn't have"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-misfired-activitylog"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739766"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# An activity log alert fired when it shouldn't have

[Activity Log alerts](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-activity-log-alerts?toc=/azure/azure-monitor/toc.json) monitor activity logs for your subscription and notify you if any activity log events match the condition set up in your alert rule.

## **Recommended Steps**

If you believe your activity log alert shouldn't have triggered but it did, the following steps may help resolve the issue.

1. Review if your activity log alert rule condition is too broad for what you want to monitor:

    * For each Azure operation (as defined by an Operation Name), there are multiple events in your activity logs with different status such as "Started", "Succeeded" or "Failed"
    * If your alert has any of the fields set to match multiple values or All, you will receive multiple alerts - one for each event matched

2. Review your activity log alert rule to check if the resource scope matches your intended resource:

    * Activity log alerts can also be set at resource group or subscription level, which could trigger the alert for when any resource in the resource group or subscription has matching activity logs

3. Review your activity logs for events that might match the condition in your alert rule:

    * Go to [activity logs in Azure Monitor](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/activityLog)
    * Filter to the resource, resource group, or subscription for which your alert was triggered (you can get this information from your alert email or under [alerts in Azure Monitor](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2))
    * Filter to around the time you saw the issue
    * Set any other filters as you might have defined in your alert rule such as Resource Type, Operation Name, Status, Event Initiated By (Caller)
    * If you find any events with this selection, it is likely the alert triggered because one of these matched the alert rule

## **Recommended Documents**

* [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
* [How to view/edit activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log)
