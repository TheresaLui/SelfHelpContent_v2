<properties
	pageTitle="I am having issues creating, editing, or deleting log alert rules"
	description="I am having issues creating, editing, or deleting log alert rules"
	infoBubbleText=""
	service="microsoft.insights"
	resource="scheduledqueryrules"
	authors="snehithm, msvijayn"
	ms.author="snmuvva, vinagara"
	displayOrder="8"
	articleId="alertarm-ai-log"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629630"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues creating, editing, or deleting log alert rules

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data for your [Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/analytics) component.

## **Recommended Steps**

If you are running into issues deploying log alerts using Azure resource manager (ARM) templates, the following steps may help resolve the issue.

1. Review the template to ensure you are passing the all the parameters correctly:

    * Alerting service requires the resource template to provide specific parameters with correct data. You can reference the [scheduledQueryRules API guide](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/) to understand the various required parameters as well as their expected input.
    * You can check the syntax of your resource template with [sample Azure resource templates for creating log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-azure-resource-template)

2. Alert rule creation using resource template can be done only if user has appropriate rights and permissions:

    * Azure Monitor has built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) to help limit access to resources while still enabling those responsible for monitoring infrastructure to obtain and configure alert rules
    * To create log alert rules, a user must have [Monitoring Contributor Role](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)<br>
