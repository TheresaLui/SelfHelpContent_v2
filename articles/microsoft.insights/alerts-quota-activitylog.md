<properties
    pageTitle="Increase activity log alert rules quota"
    description="I need to increase my quota of activity log alert rules"
    infoBubbleText=""
    service="microsoft.insights"
    resource="activityLogAlerts"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-quota-activitylog"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739772"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I need to increase my quota of activity log alert rules 

## **Recommended Steps**

In a subscription up to 100 alert rules can be created for an activity of scope at either: a single resource, all resources in resource group (or) entire subscription level.
A solution is to import the activity log into the log analytics workspace and use log search alerts instead. See information on importing activity log into Log Analytics workspace here.
In a subscription up to 100 alert rules can be created for an activity of scope at either: a single resource, all resources in resource group (or) entire subscription level.
A solution is to import the activity log into the log analytics workspace and use log search alerts instead. See information on importing activity log into Log Analytics workspace [here](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts).

## **Recommended Documents**

* [Alerts on activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
