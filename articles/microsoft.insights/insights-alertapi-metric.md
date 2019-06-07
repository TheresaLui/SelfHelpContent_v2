<properties
	pageTitle="I am having issues managing Metric alerts with API/CLI"
	description="I am having issues managing Metric alerts with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="8"
	articleId="insights-alertapi-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629618"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax"
/>

# I am having issues managing metric alerts with API/CLI

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating/deleting metric alerts using REST API or Azure command line interface (CLI), the following steps may help resolve the issue.

1. Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/metricalerts/) to verify you are passing the all the parameters correctly.

2. Review you are using the right CLI commands for metric alerts.
    * CLI commands for metric alerts start with `az monitor metrics alert`. Review the [Azure CLI reference](https://docs.microsoft.com/cli/azure/monitor/metrics/alert?view=azure-cli-latest) to learn about the syntax.
    * You can see [sample showing how to use metric alert CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli).

3. If you are receiving a `Metric  not found` error, ensure you are using the Metric name from [this page](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and not the Metric Display Name.

4. Review if you have appropriate permissions. To create/update/delete metric alerts
    * you should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or
    * you should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts.

## Known Issues

1. PowerShell cmdlets for new metric alerts are not yet available but will be available by end of March 2019.

2. Azure CLI doesn't yet support creating [multi-resource metric alerts](https://azure.microsoft.com/blog/monitor-at-scale-in-azure-monitor-with-multi-resource-metric-alerts/).

3. Azure CLI doesn't yet support managing [metric alerts with Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds).