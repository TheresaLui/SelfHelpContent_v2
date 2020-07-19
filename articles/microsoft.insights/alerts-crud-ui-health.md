<properties
    pageTitle="Issues configuring service health or resource health alert rules in the Azure portal"
    description="I'm trying to create, edit or delete a Service health or resource health alert rule, but I'm getting an error, or I don't know how to configure it"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-crud-ui-health"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739806"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# **I have an issue in creating, editing or deleting Service or Resource Health alert rules in the Azure portal**

## Resource health

Azure Resource Health alerts tracks the health of your resources, it tracks resource health events and allow you to be notified in near real-time when there's a change in the resources health status.

## Service health

Azure Service Health tracks the health of your Azure services in the regions where you use them. You can set up activity log alerts on Service Health events to get notified of ongoing service issues, upcoming planned maintenance, or relevant health advisories.


## **Recommended Steps**

If you are facing issues while trying to setup activity log alerts, please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert.
    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) to author alerts on it.
2. You can create or update "Resource health" alerts on the portal as documented [here](https://docs.microsoft.com/azure/service-health/resource-health-alert-monitor-guide)
3. You can create or update "Service heath" alerts on the portal as documented [here](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications?toc=%2Fazure%2Fservice-health%2Ftoc.json).
