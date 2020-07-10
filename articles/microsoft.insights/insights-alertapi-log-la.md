<properties
	pageTitle="I am having issues managing Log alerts with API/CLI"
	description="I am having issues managing Log alerts with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="scheduledqueryrules"
	authors="snehithm, msvijayn"
	ms.author="snmuvva, vinagara"
	displayOrder="8"
	articleId="insights-alertapi-log-la"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629617,32633014"
	resourceTags=""
	productPesIds="15454,15725"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues managing Log alerts with API/CLI

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data available on [Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/log-query/query-language).

## **Recommended Steps**

If you are running into issues creating/updating log alerts using REST API or Azure command line interface (CLI), the following steps may help resolve the issue.

1. Review which REST API you are using to manage your log alerts:

    * [ScheduledQueryRules API](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/) is the recommended API to manage log alerts in Azure Monitor
    * However, to ensure backward compatibility with legacy OMS systems, [legacy Log Analytics Alert API](https://docs.microsoft.com/azure/azure-monitor/platform/api-alerts) is still supported
    * Alerts created through one of the APIs above can only be updated using the same API
    * Unless you have [explicitly switched](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch) to use new API only, rules created in the portal will be created using the legacy Log Analytics Alert API

2. Review if you are using legacy API to manage rules with newer functionality:

    * Rules with [following functionality](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch#benefits-of-switching-to-new-azure-api) is only supported via new Azure Monitor - ScheduledQueryRules API (cross-resource queries, time period greater than 24 hours, specifying which group field to aggregate-on (for metric measurement type rules) etc.)

3. Currently, Azure Monitor Log Alerts does not have native CLI commands:

    * It is recommended to use Azure Resource Manager CLI commands instead for deploying log alert rules
    * For details, see [sample log alert creation using Azure Resource Manager CLI command](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-powershell-cli-or-api)

4. Review if you have appropriate permissions. To create/update/delete log alerts:

    * You should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)<br>
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)<br>
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)<br>
