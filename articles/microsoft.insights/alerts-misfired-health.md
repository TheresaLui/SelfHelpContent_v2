<properties
    pageTitle="A service health or a resource health alert fired when it shouldn't have"
    description="A service health or a resource health alert fired when it shouldn't have"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-misfired-health"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739808"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# A service health or a resource health alert fired when it shouldn't have

## Resource health

Azure Resource Health alerts tracks the health of your resources. They track resource health events and allow you to be notified in near real-time when there's a change in the resource health status.

## Service health

Azure Service Health tracks the health of your Azure services in the regions where you use them. You can set up activity log alerts on Service Health events to get notified of ongoing service issues, upcoming planned maintenance, or relevant health advisories.

## **Recommended Steps**

If you believe your resource or service health alert shouldn't have triggered but it did, the following steps might help resolve the issue.

1. Review if your resource or service health alert rule condition is too broad for what you want to monitor:
    * For each Azure operation (as defined by an Operation Name), there are multiple events in your activity logs with different status such as "Started", "Succeeded" or "Failed"
    * If your alert has any of the fields set to match multiple values or All, you will receive multiple alerts - one for each event matched
        1. In service health: Review if the Services, Regions, Event types in your rule match the services, regions and event type you were expecting the notification for.
        2. In resource health: Resource Health Alerts are not currently supported through the portal, You can create Resource Health alerts through ARM template as described here. In "Resource Health" alerts ARM template there are several of parameters (for example: "Resource Status" and "Event status") only events that have the same parameters values as it was defined in the rule will be detected.
2. Review your activity log alert rule to check if the resource scope matches your intended resource:
    * Activity log alerts can also be set at resource group or subscription level, which could trigger the alert for when any resource in the resource group or subscription has matching activity logs
3. Review your activity logs for events that might match the condition in your alert rule:
    * Go to activity logs in Azure Monitor
    * Filter to the resource, resource group, or subscription for which your alert was triggered (you can get this information from your alert email or under alerts in Azure Monitor)
    * Filter to around the time you saw the issue
    * Set any other filters as you might have defined in your alert rule such as Resource Type, Operation Name etc.
    * If you find any events with this selection, it is likely the alert triggered because one of these matched the alert rule

## **Recommended Documents**

* [How to view/edit activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log)
* [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json)
* [Configure health notifications for existing problem management systems using a webhook](https://docs.microsoft.com/azure/service-health/service-health-alert-webhook-guide)
* [Azure Resource Health Overview](https://docs.microsoft.com/azure/service-health/resource-health-overview)
* [Azure Resource Health FAQs](https://docs.microsoft.com/azure/service-health/resource-health-faq)
