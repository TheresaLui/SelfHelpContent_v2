<properties
    pageTitle="Action rule is not working as expected"
    description="My action rule did not suppress all action groups or did not add an action group correctly, or did something unexpected"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="8"
    articleId="alert-notifications-action-rule"
    selfHelpType="generic"
    supportTopicIds="32739764"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# Action rule is not working as expected

## **Recommended Steps**

If you can see a fired alert in the portal, but a related [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) did not work as expected, follow these steps:

**1. Is the action rule enabled?**

Check the action rule status column to verify that the related action role is enabled.

![action rule status in the alert list](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/action-rule-status.png)

If it is not enabled, you can enable the action rule by selecting it and clicking Enable.

**2. Is it a service health alert?**

Service health alerts (monitor service = "Service Health") are not affected by action rules.

**3. Did the action rule act on your alert?**

Check if the action rule has processed your alert by clicking on the fired alert in the portal, and look at the history tab.

Here is an example of action rule suppressing all action groups:

![Alert details history with action rule suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)

Here is an example of an action rule adding another action group:

![Alert details history tab with action group added by an action rule](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/action-repeated-multi-action-groups.png)

**4. Does the action rule scope and filter match the fired alert?**

If you think the action rule should have fired but didn't, or that it shouldn't have fired but it did, carefully examine the action rule scope and filter conditions versus the properties of the fired alert.
