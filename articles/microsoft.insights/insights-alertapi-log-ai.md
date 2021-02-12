<properties
	pageTitle="I am having issues managing Log alerts with API/CLI"
	description="I am having issues managing Log alerts with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="scheduledqueryrules"
	authors="snehithm, msvijayn"
	ms.author="snmuvva, vinagara"
	displayOrder="8"
	articleId="insights-alertapi-log-ai"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629616"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues managing Log alerts with API/CLI

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data for your [Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/analytics) component.

## **Recommended Steps**

If you are running into issues deploying log alerts using REST API or Azure command line interface (CLI), the following steps may help resolve the issue.

1. Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/) to verify you are passing the all the parameters correctly
2. Currently, Azure Monitor Log Alerts does not have native CLI commands:

    * It is recommended to use Azure Resource Manager CLI commands instead for deploying log alert rules
    * For details, see [sample log alert creation using Azure Resource Manager CLI command](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-powershell-cli-or-api)

3. Review if you have appropriate permissions. To create/update/delete log alerts:

    * You should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)<br>
