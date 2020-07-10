<properties
	pageTitle="I am having issues with ARM templates for log alert rules"
	description="I am having issues with ARM templates for log alert rules"
	infoBubbleText=""
	service="microsoft.insights"
	resource="scheduledqueryrules"
	authors="snehithm, msvijayn"
	ms.author="snmuvva, vinagara"
	displayOrder="8"
	articleId="insights-alertarm-log-la"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629631,32612430"
	resourceTags=""
	productPesIds="15454,15725"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues with ARM templates for log alert rules

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data available on [Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/log-query/query-language).

## **Recommended Steps**

If you are running into issues deploying log alerts using Azure resource manager (ARM) templates, the following steps may help resolve the issue.

1. If workspace is not found, ensure alert rule 'location' parameter matches the location of the workspace
2. Ensure you are using the correct variant of resource template for log alert:

    * Alerting service in Azure Monitor uses the [scheduledQueryRules API](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/). You can check the syntax of your resource template with [sample Azure resource templates for creating log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-azure-resource-template).
    * To ensure backward compatibility with legacy OMS systems, Log alerts for Log Analytics can also be created using the [legacy Log Analytics Alert API](https://docs.microsoft.com/azure/azure-monitor/platform/api-alerts). If you are using the legacy API structure, you can compare the syntax of your resource template with [sample Azure resource templates](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-resources-searches-alerts#alerts).
    * Newer functionality like [support for cross-resource queries, time period of up to 48 hours, specify which group field to aggregate-on, etc.](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch#benefits-of-switching-to-new-azure-api) are only available via new Azure Monitor - ScheduledQueryRules API and resource template

3. Alert rule creation using resource template can be done only if user has appropriate rights and permissions:

	* Azure Monitor has built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) to help limit access to resources while still enabling those responsible for monitoring infrastructure to obtain and configure alert rules
    * To create log alert rules, a user must have [Monitoring Contributor Role](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)<br>
