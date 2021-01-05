<properties
  pagetitle=""
  service="microsoft.insights"
  resource="activitylogalerts"
  ms.author="t-yasaya"
  selfhelptype="Generic"
  supporttopicids="32739806"
  resourcetags=""
  productpesids="15454"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-crud-ui-health"
  ownershipid="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts" />
## **I have an issue in creating, editing or deleting Service or Resource Health alert rules in the Azure portal**

**1.	I am not sure what is the difference between Service Health alert and Resource Health alert, or how to configure it.**

[Service Health](https://docs.microsoft.com/en-us/azure/service-health/service-health-overview) tracks the health of Azure services across the subscriptions and regions in which you operate.
You can [configure Service Health alert rules](https://docs.microsoft.com/en-us/azure/service-health/alerts-activity-log-service-notifications-portal) to get notified of ongoing service issues, upcoming planned maintenance, or relevant health / security advisories, that has impact on you.

[Resource Health](https://docs.microsoft.com/en-us/azure/service-health/resource-health-overview) tracks the health of your specific Azure resources.
You can [configure Resource Health alert rules](https://docs.microsoft.com/en-us/azure/service-health/resource-health-alert-monitor-guide) to get notified when there are changes in your resource’s health status, for example: when a specific virtual machine becomes unavailable.



**2.	I created an alert rule, but don’t see it in the portal.**
Existing alert rules can be reviewed in Monitor>Alerts>Manage Alert Rules.
Service Health alert rules can also be reviewed in Service Health>Health Alerts.



**3.	I am not sure if I have the permissions to author the alert.**
You are required to have the role of [monitoring contributor](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/roles-permissions-security?WT.mc_id=Portal-Microsoft_Azure_Support#built-in-monitoring-roles) on the target subscription to author alerts on it.