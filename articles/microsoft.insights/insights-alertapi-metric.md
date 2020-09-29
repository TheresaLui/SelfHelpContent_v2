<properties
	pageTitle="I am having issues managing Metric alerts with API/CLI"
	description="I am having issues managing Metric alerts with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="insights-alertapi-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629618"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues managing metric alerts with API/CLI

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating/deleting metric alerts using REST API, PowerShell or Azure command line interface (CLI), the following steps may help resolve the issue.

1. Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/metricalerts/) to verify you are passing the all the parameters correctly
2. Review you are using the right CLI commands for metric alerts:

    * CLI commands for metric alerts start with `az monitor metrics alert`. Review the [Azure CLI reference](https://docs.microsoft.com/cli/azure/monitor/metrics/alert?view=azure-cli-latest) to learn about the syntax
    * You can see [sample showing how to use metric alert CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli)
    * To alert on a custom metric, make sure to prefix the metric name with the relevant metric namespace: NAMESPACE.METRIC

3. Review you are using the right PowerShell cmdlets for metric alerts:

    * PowerShell cmdlets for metric alerts are available in the [Az.Monitor module](https://docs.microsoft.com/powershell/module/az.monitor/?view=azps-3.2.0#monitor)
    * Make sure to use the cmdlets ending with V2 for new (non-classic) metric alerts (e.g. [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/Add-AzMetricAlertRuleV2?view=azps-3.2.0))

4. If you are receiving a `Metric  not found` error, ensure you are using the Metric name from [this page](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and not the Metric Display Name
5. Review if you have appropriate permissions. To create/update/delete metric alerts:

    * You should have been assigned a built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
    * You should have been assigned a [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

### Known Issues

1. Azure CLI doesn't yet support creating [multi-resource metric alerts](https://azure.microsoft.com/blog/monitor-at-scale-in-azure-monitor-with-multi-resource-metric-alerts/)
2. Azure CLI doesn't yet support managing [metric alerts with Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)
