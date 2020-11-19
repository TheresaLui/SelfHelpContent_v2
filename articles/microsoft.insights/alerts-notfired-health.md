<properties
    pageTitle="A service or resource health alert wasn't fired when it should"
    description="A service or resource health alert wasn't fired when it should"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-notfired-health"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739809"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# **A service or resource health alert wasn't fired when it should**

## Resource health

Azure Resource Health alerts tracks the health of your resources, it tracks resource health events and allow you to be notified you in near real-time when there's change in the resource health status.

## Service health

Azure Service Health tracks the health of your Azure services in the regions where you use them. You can set up activity log alerts on Service Health events to get notified of ongoing service issues, upcoming planned maintenance, or relevant health advisories.

## **Recommended Steps**

### Service Health

If you believe your "Service Health" alert should have triggered but it didn't, the following steps might help resolve the issue.

1. Review the [fired alerts list](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see if an alert was fired for your alert rule. If you can see the alert in the portal, then the issue might be with notification.

    * Check if you have any rules that might prevent receiving emails from Azure emails
    * If you are using Webhook, check if your webhook receiver accepts the payload sent by activity log alerts

2. Review your activity logs for events that might match the condition in your alert rule:

    * Go to activity logs in Azure Monitor
    * Filter to the resource, resource group, or subscription for which your alert was supposed to trigger
    * Filter to around the time you saw the issue
    * Set all other filters as you might have defined in your alert rule such as Resource Type, Operation Name, Status, Event Initiated By (Caller)
    * If you do not find any events that match your filters, it is likely why the alert didn't trigger

3. Review if your activity log alert rule condition is too strict for what you want to monitor:

    * For each Azure operation (as defined by an Operation Name), there are multiple events in your activity logs with different status such as "Started", "Succeeded" or "Failed". If your rule matches a rarer condition like when Status is "Failed", you will not get an alert for events with Status as "Succeeded" or "Started"
    * If you believe you should have received a Service Health notification but haven't, then:

        1. Review if the Services in your rule match the services you were expecting the notification for
        2. Review if the Regions in your rule match the regions where you use the Azure services
        3. Review if the Event type in your rule matches the event type of the Service Health event

### Resource health 

If you believe your "Resource Health" alert should have triggered but it didn't, the following steps might help resolve the issue.

1. Fired alerts for resource health alert rules are not displayed in fired alerts list, you can only get notified by using action groups.
    * Check if you have any rules that might prevent receiving emails from Azure emails
    * If you are using Webhook, check if your webhook receiver accepts the payload sent by activity log alerts
2. Review your activity logs for events that might match the condition in your alert rule:
    * Go to activity logs in Azure Monitor
    * Filter to the resource, resource group, or subscription for which your alert was supposed to trigger
    * Filter to around the time you saw the issue
3. Notice that: Service health alerts does not send an alert regarding resource health events
    * Set all other filters as you might have defined in your alert rule such as Resource Type, Operation Name, Status, Event Initiated By (Caller)
    * If you do not find any events that match your filters, it is likely why the alert didn't trigger
4. Review if your activity log alert rule condition is too strict for what you want to monitor:
    * For each Azure operation (as defined by an Operation Name), there are multiple events in your activity logs with different status such as "Started", "Succeeded" or "Failed". If your rule matches a rarer condition like when Status is "Failed", you will not get an alert for events with Status as "Succeeded" or "Started"
    * Resource Health Alerts is not currently supported through the portal, You can create Resource Health alerts through ARM template as described here. In "Resource Health" alerts ARM template there are several of parameters (for example: "Resource Status" and "Event status") only events that have the same parameters values as it was defined in the rule will be detected.

## **Recommended Documents**

* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json)
* [Configure health notifications for existing problem management systems using a webhook](https://docs.microsoft.com/azure/service-health/service-health-alert-webhook-guide)
* [Azure Resource Health Overview](https://docs.microsoft.com/azure/service-health/resource-health-overview)
* [Azure Resource Health FAQs](https://docs.microsoft.com/azure/service-health/resource-health-faq)
