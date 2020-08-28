<properties
  pagetitle="**I have an issue in creating, editing or deleting activity log alert rules in the Azure portal**"
  service="microsoft.insights"
  resource="activitylogalerts"
  ms.author="nolavime,aaronmax"
  selfhelptype="Generic"
  supporttopicids="32739771"
  resourcetags=""
  productpesids="15454"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-crud-ui-activitylog"
  ownershipid="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts" />
# **I have an issue in creating, editing or deleting activity log alert rules in the Azure portal**

## **Recommended Steps**

You can create activity log alerts on the portal as documented [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log).

If you are facing issues while trying to setup activity log alerts, please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert:
    
    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) in order to author alerts on it
    
2. Verify if the event that you wish to get alerted on is in the [list of supported ARM operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations)
3. On the Azure portal, you can create an activity log alert from the alerts blade or from the activity logs blade in [Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#azure-portal):

    * From the alerts blade, select new alert rule. You now have to define the target (which could be a resource/resource group/subscription) and define the criteria that you want to be alerted for (e.g. "All administrative operations"). The next step is to assign an action group for the alert rule, and provide a name and description for the alert rule.
    * Alternatively, you can select the activity log you want to be alerted for from the [activity logs in Azure Monitor](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/activityLog) blade and select the "Add activity log alert" button. This opens up the alert creation experience from the previous step, with the alert target and criteria pre-configured.

For viewing your alerts, you can go to [Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#azure-portal) and select the Alerts blade. From there, selecting "Manage alert rules" will take you to a listed view of all your configured alert rules. You can select an alert rule to open up more information about it. From this page, you can modify, enable/disable, and delete the alert rule.

### **Advisory and How-To**
[![Monitoring Video](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/alerts/how-to-configure-an-alert-rule.png)](https://www.microsoft.com/videoplayer/embed/RE4tflw?autoplay=1)