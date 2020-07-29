<properties
    pageTitle="Action or notification has an unexpected content"
    description="I received the alert, but some of its fields are missing or incorrect"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="7"
    articleId="alerts-notification-unexpected-content"
    selfHelpType="generic"
    supportTopicIds="32739762"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# I received an action or notification with an unexpected content

## **Recommended Steps**

If you have received the alert, but believe some of its fields are missing or incorrect, follow these steps:

**1. Did you pick the correct format for the action?**

Each action type (email, webhook, etc.) has two formats – the default, legacy format, and the newer [common schema format](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-common-schema). When you create an action group, you specify the format you want per action – different actions in the action groups may have different formats.



For example, for webhook action:
![webhook action schema option](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/webhook.png)

Check if the format specified at the action level is what you expect. For example, you may have developed code that responds to alerts (webhook, function, logic app, etc.), expecting one format, but later in the action you or another person specified a different format.

Also, check the payload format (JSON) for [activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts-webhook), for [log search alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-webhook) (both Application Insights and log analytics), for [metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time#payload-schema), for the [common alert schema](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-common-schema-definitions), and for the deprecated [classic metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks).

**2. Activity log alerts: Is the information available in the activity log?**

[Activity log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts) are alerts that are based on events written to the Azure Activity Log. For example, this includes events about creating, updating or deleting Azure resources, service health and resource health events, or findings from Azure Advisor and Azure Policy. 

If you have received an alert based on the activity log but some fields that you need are missing or incorrect, first check the events in the activity log itself. If the Azure resource did not write the fields you are looking for in its activity log event, those fields will not be included in the corresponding alert.

