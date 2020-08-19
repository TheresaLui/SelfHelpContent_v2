<properties
	pageTitle="Creating, editing, or deleting activity log alert rules"
	description="Creating, editing, or deleting activity log alert rules"
	infoBubbleText=""
	service="microsoft.insights"
	resource="activitylogalerts"
	authors="snehithm, msvijayn,anantr"
	authoralias="snmuvva, vinagara, anantr"
	displayOrder="7"
	articleId="insights-alertcrud-activity-log"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629622"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# Creating, editing, or deleting activity log alert rules

You can create activity log alerts on the portal as documented [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log).

## **Recommended Steps**

If you are facing issues while trying to setup activity log alerts, please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert.
    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com//azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) to author alerts on it.

2. Verify if the event that you wish to get alerted on is in the [list of supported ARM operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations).

3. On the Azure portal, you can create an activity log alert from the alerts blade or from the activity logs blade in [Azure Monitor](https://docs.microsoft.com//azure/azure-monitor/platform/alerts-activity-log#azure-portal).
    * From the alerts blade, select new alert rule. You now have to define the target (which could be a resource/resource group/subscription) and define the criteria that you want to be alerted for (e.g. "All administrative operations"). The next step is to assign an action group for the alert rule, and provide an name and description for the alert rule.
    * Alternatively, you can select the activity log you want to be alerted for from the activity log blade and select the "Add activity log alert" button. This opens up the alert creation experience from the previous step, with the alert target and criteria pre-configured.

For viewing your alerts, you can go to Azure Monitor and select the Alerts blade. From there, selecting "Manage alert rules" will take you to a listed view of all your configured alert rules. You can select an alert rule to open up more information about it. From this page, you can modify, enable/disable and delete the alert rule.