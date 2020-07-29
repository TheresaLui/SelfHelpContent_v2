<properties
	pageTitle="I am having issues managing metric alerts using ARM templates, REST API, PowerShell or CLI"
	description="I am having issues managing metric alerts using ARM templates, REST API, PowerShell or CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-crud-api-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739796"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I am having issues managing metric alerts using ARM templates, REST API, PowerShell, or CLI

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating/deleting metric alerts using ARM templates, REST API, PowerShell, or the Azure command line interface (CLI), the following steps may help resolve the issue.

### ARM templates

1. Review the [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly
2. Refer to the [metric alerts ARM template examples](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates) to ensure you are passing the all the parameters correctly

### REST API

* Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/metricalerts/) to verify you are passing the all the parameters correctly

### PowerShell

Ensure you are using the right PowerShell cmdlets for metric alerts:

* PowerShell cmdlets for metric alerts are available in the [Az.Monitor module](https://docs.microsoft.com/powershell/module/az.monitor/?view=azps-3.6.1)
* Make sure to use the cmdlets ending with V2 for new (non-classic) metric alerts (e.g. [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/Add-AzMetricAlertRuleV2?view=azps-3.6.1))
	
### CLI

Ensure you are using the right CLI commands for metric alerts:

* CLI commands for metric alerts start with `az monitor metrics alert`. Review the [Azure CLI reference](https://docs.microsoft.com/cli/azure/monitor/metrics/alert?view=azure-cli-latest) to learn about the syntax.
* You can see [sample showing how to use metric alert CLI](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric#with-azure-cli)
* To alert on a custom metric, make sure to prefix the metric name with the relevant metric namespace: NAMESPACE.METRIC

### General

1. If you are receiving a `Metric not found` error:
	
	- For a platform metric, make sure that you are using the **Metric** name from [this page](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and not the **Metric Display Name**
	- For a custom metric, make sure that the metric is already being emitted (you cannot create an alert rule on a custom metric that doesn't yet exist), and that you are providing the custom metric's namespace (see an ARM template example [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-static-threshold-metric-alert-that-monitors-a-custom-metric))
2. If you are creating [metric alerts on logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs), ensure appropriate dependencies are included. See [sample template](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#resource-template-for-metric-alerts-for-logs).
3. If you are creating an alert rule that contains multiple criteria, please note the following constraints:

	- You can only select one value per dimension within each criterion
	- You cannot use "\*" as a dimension value
	- When metrics that are configured in different criterions support the same dimension, then a configured dimension value must be explicitly set in the same way for all of those metrics (see an ARM template example [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-static-threshold-metric-alert-that-monitors-multiple-criteria))

4. Review if you have appropriate permissions. To create/update/delete metric alerts:

	* You should have been assigned a built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor), or
	* You should have been assigned a [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

### Known Issues

1. Azure CLI doesn't yet support creating [multi-resource metric alerts](https://azure.microsoft.com/blog/monitor-at-scale-in-azure-monitor-with-multi-resource-metric-alerts/)
2. Azure CLI doesn't yet support managing [metric alerts with Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)

## **Recommended Documents**

* [How metric alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
* [Metric alerts template reference](https://docs.microsoft.com/azure/templates/microsoft.insights/2018-03-01/metricalerts)
