<properties
    pageTitle="Action or notification happened more than once"
    description="I have a specific alert that its notification or action triggered multiple times"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="5"
    articleId="alerts-notification-multiple-trigger"
    selfHelpType="generic"
    supportTopicIds="32739760"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# I received an action or notification more than once

## **Recommended Steps**

If you have received a notification for an alert (such as an email or an SMS) more than once, or the alert's action (such as webhook or Azure function) was triggered multiple times, follow these steps:

**1. Is it really the same alert?**

In some cases, multiple similar alerts are fired at around the same time. So, it might just seem like the same alert triggered its actions multiple times. For example, an activity log alert rule might be configured to fire both when an event has started, and when it has finished (succeeded or failed), by not filtering on the event status field.

To check if these actions or notifications came from different alerts, examine the alert details, such as its timestamp and either the alert id or its correlation id. Alternatively, check the list of fired alerts in the portal. If these are different alerts, you might need to adapt the alert rule logic or otherwise configure the alert source.

**2. Does the action repeat in multiple action groups?**

When an alert is fired, each of its action groups is processed independently. So, if an action (such as an email address) appears in multiple triggered action groups, it would be called once per action group.

To check which action groups were triggered, check the alert history tab. You would see there both action groups defined in the alert rule, and action groups added to the alert by [action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules):

![alert details history tab with multiple action groups](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/action-repeated-multi-action-groups.png)
