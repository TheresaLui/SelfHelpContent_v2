<properties
	pageTitle="I am having problems with Activity Log Alerts API/CLI"
	description="I am having problems with Activity Log Alerts API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="activitylogalerts"
	authors="snehithm, msvijayn,anantr"
	ms.author="snmuvva, vinagara, anantr"
	displayOrder="7"
	articleId="insights-alertarm-activity-log"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629629"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having problems with Activity Log Alerts API/CLI

You can create activity log alerts using the REST API or CLI as documented [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#azure-resource-template).

## **Recommended Steps**

If you are facing issues while trying to setup activity log alerts using the REST API or CLI, please use the following steps to troubleshoot:

1. Ensure you have the appropriate permissions to author the alert:

    * You are required to have the role of [monitoring contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#built-in-monitoring-roles) on the target resource (or resource group/subscription) to author alerts on it

2. Verify if the event that you wish to get alerted on is in the [list of supported ARM operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations)
3. Verify that you have used the appropriate syntax as defined [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-activity-log#azure-resource-template)
