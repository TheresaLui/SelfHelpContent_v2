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

* In a single subscription, up to 100 alertactivity log rules can be created for scope at either: a single resource, all resources in resource group, or the entire subscription level
* If more than a 100 rules are needed, a solution could be to import the activity log into your log analytics workspace and use log search alerts instead. See information on importing activity log into Log Analytics workspace [here](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts).

## **Recommended Documents**

* [Alerts on activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log-alerts)
