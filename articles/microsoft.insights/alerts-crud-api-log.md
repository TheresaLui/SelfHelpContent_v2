<properties
    pageTitle="I am having issues managing Log alerts with API, CLI or ARM template"
    description="I am having issues managing Log alerts with API, CLI or ARM template"
    infoBubbleText=""
    service="microsoft.insights"
    resource="scheduledqueryrules"
    authors="yalavi"
    ms.author="yalavi"
    displayOrder="8"
    articleId="alerts-crud-api-log"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739786,32612430,32633014"
    resourceTags=""
    productPesIds="15454,15725"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_LogSearchAlerts"
/>

# I am having issues managing Log alerts with API, CLI or ARM template

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data available on [Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/log-query/query-language).

## **Recommended Steps**

If you are running into issues creating/updating log alerts using REST API or Azure command line interface (CLI), the following steps may help resolve the issue.

1. Review which REST API you are using to manage your log alerts:

    * [ScheduledQueryRules API](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/) is the recommended API to manage log alerts in Azure Monitor. You can check the syntax of your resource template with [sample Azure resource templates for creating log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-azure-resource-template).
    * For older workspaces, there is backward compatibility with legacy OMS systems, [legacy Log Analytics Alert API](https://docs.microsoft.com/azure/azure-monitor/platform/api-alerts). If you are using the legacy API structure, you can compare the syntax of your resource template with [sample Azure resource templates](https://docs.microsoft.com/azure/azure-monitor/insights/solutions-resources-searches-alerts#alerts).
    * Alerts created through one of the APIs above can only be updated using the same API

2. Review if you are using legacy API to manage rules with newer functionality:

    * Rules with following functionality are only supported via new Azure Monitor - ScheduledQueryRules API; PowerShell cmdlets, cross-resource queries, time period greater than 24 hours, specifying which field to aggregate-on (for metric measurement type rules). [Learn how to switch APIs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch#benefits-of-switching-to-new-azure-api).

3. Currently, Azure Monitor Log Alerts does not have native CLI commands:

    * It is recommended to use Azure Resource Manager CLI commands instead for deploying log alert rules
    * For details, see [sample log alert creation using Azure Resource Manager CLI command](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-using-cli-or-api)

4. Review if you have appropriate permissions. To create/update/delete log alerts:

    * You should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)
