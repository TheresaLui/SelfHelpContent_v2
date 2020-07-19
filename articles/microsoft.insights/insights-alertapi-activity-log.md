<properties
	pageTitle="I am having problems with Activity Log Alerts API/CLI"
	description="I am having problems with Activity Log Alerts API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="activitylogalerts"
	authors="snehithm, msvijayn,anantr"
	ms.author="snmuvva, vinagara, anantr"
	displayOrder="7"
	articleId="insights-alertapi-activity-log"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629615"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having problems with Activity Log Alerts API/CLI

You can create activity log alerts using the [REST API](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#rest-api) or [CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#cli).

## **Recommended Steps**

If you are facing issues while trying to setup activity log alerts using the REST API or CLI, please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert: 

    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) to author alerts on it

2. Verify if the event that you wish to get alerted on is in the [list of supported ARM operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations)

3. Verify that you have used the appropriate syntax for the [REST API](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#rest-api), [PowerShell](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#powershell) and [CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#cli)

    * When authoring using CLI, you are required to do three steps (in the following order): [Create a new activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert#az-monitor-activity-log-alert-create), [Assign a scope for the activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert/scope), [Assign an action group to the activity log alert rule](https://docs.microsoft.com/cli/azure/monitor/activity-log/alert/action-group)
    
