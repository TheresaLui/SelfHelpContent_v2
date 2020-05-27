<properties
	pageTitle="I am having issues with Metric alerts ARM templates"
	description="I am having issues with Metric alerts ARM templates"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="insights-alertarm-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629632"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues with metric alerts ARM templates

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating metric alerts using Azure Resource Manager (ARM) templates, the following steps may help resolve the issue:

1. Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly
2. Review the template to ensure you are passing the all the parameters correctly. See [some samples](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-more-advanced-static-threshold-metric-alert) for metric alert templates.
3. If you are receiving a `Metric not found` error:
	- For a platform metric - Make sure that you are using the **Metric** name from [this page](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and not the **Metric Display Name**
	- For a custom metric - Make sure that the metric is already being emitted (you cannot create an alert rule on a custom metric that doesn't yet exist), and that you are providing the custom metric's namespace (see example [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-static-threshold-metric-alert-that-monitors-a-custom-metric))
4. If you are creating [metric alerts on logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs), ensure appropriate dependencies are included. See [sample template](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#resource-template-for-metric-alerts-for-logs).
5. Please note the following constraints when using dimensions in an alert rule that contains multiple criteria:

	- You can only select one value per dimension within each criterion
	- You cannot use "\*" as a dimension value
	- When metrics that are configured in different criterions support the same dimension, then a configured dimension value must be explicitly set in the same way for all of those metrics (see an example [here](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-static-threshold-metric-alert-that-monitors-multiple-criteria))

6. Review if you have appropriate permissions. To create/update/delete metric alerts:

    * You should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or
    * You should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

## **Recommended Documents**

* [How metric alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
* [Metric alerts template reference](https://docs.microsoft.com/azure/templates/microsoft.insights/2018-03-01/metricalerts)
