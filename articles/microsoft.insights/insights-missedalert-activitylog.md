<properties
	pageTitle="My activity log alert didn't fire when it should have"
	description="My activity log alert didn't fire when it should have"
	infoBubbleText=""
	service="microsoft.insights"
	resource="activitylogalerts"
	authors="snehithm, msvijayn"
	authoralias="snmuvva, vinagara"
	displayOrder="7"
	articleId="missedalert-activitylog"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629635,32629640"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, mooncake"
/>

# My activity log alert didn't fire when it should have

[Activity Log alerts](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-activity-log-alerts?toc=/azure/azure-monitor/toc.json) monitor activity logs for your subscription and notify you if any activity log events match the condition set up in your alert rule.

## **Recommended Steps**

If you believe your activity log alert should have triggered but it didn't, the following steps might help resolve the issue.

1. Review the [fired alerts list](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see if an alert was fired for your alert rule. If you can see the alert in the portal, then the issue might be with notifications.
   * Check if you have any rules that might prevent receiving emails from [Azure emails](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information)
   * Check if your web hook receiver accepts the [payload sent by activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts-webhook)

2. Review your activity logs for events that might match the condition in your alert rule:
    * Go to [activity logs in Azure Monitor](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/activityLog)
    * Filter to the resource, resource group, or subscription for which your alert was supposed to trigger
    * Filter to around the time you saw the issue
    * Set all other filters as you might have defined in your alert rule such as Resource Type, Operation Name, Status, Event Initiated By (Caller)
    * If you do not find any events that match your filters, it is likely why the alert didn't trigger

3. Review if your activity log alert rule condition is too strict for what you want to monitor:
    * For each Azure operation (as defined by an Operation Name), there are multiple events in your activity logs with different status such as "Started", "Succeeded" or "Failed". If your rule matches a rarer condition like when Status is "Failed", you will not get an alert for events with Status as "Succeeded" or "Started"

## **Recommended Documents**

* [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)<br>
* [How to view/edit activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log)<br>
