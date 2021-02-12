<properties
    pageTitle="ARM templates for health alerts REST API, CLI or PowerShell"
    description="I have an issue with ARM templates, REST API, CLI or PowerShell for service or health alerts"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-crud-api-health"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739807"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I have an issue with ARM templates, REST API, CLI or PowerShell for health alerts

You can create activity log alerts using the REST API, CLI or PowerShell.

## **Recommended Steps**

If you are facing issues while trying to setup activity log alerts using the [REST API](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#rest-api) or [CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#cli), please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert:
    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) to author alerts on it.
2. Verify if the event that you wish to get alerted on is in the [list of supported ARM operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations).
3. Verify that you have used the appropriate syntax for the [REST API](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#rest-api), [PowerShell](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#powershell) and [CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#cli)
    * When authoring using CLI, you are required to do three steps (in the following order): [Create a new activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert#az-monitor-activity-log-alert-create), [Assign a scope for the activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert/scope), [Assign an action group to the activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert/action-group)
4. Verify that your ARM template is with the appropriate format:
    * [Resource health](https://docs.microsoft.com/azure/service-health/resource-health-alert-arm-template-guide)
    * [Service Health](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications?toc=%2Fazure%2Fservice-health%2Ftoc.json)
