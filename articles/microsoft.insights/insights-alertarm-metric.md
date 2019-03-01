<properties
	pageTitle="I am having issues with Metric alerts ARM templates"
	description="I am having issues with Metric alerts ARM templates"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="8"
	articleId="insights-alertarm-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629632"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax"
/>

# I am having issues with metric alerts ARM templates

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you are running into issues creating/updating metric alerts using Azure Resource Manager (ARM) templates, the following steps may help resolve the issue.

1. Review [common Azure deployment errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) list and troubleshoot accordingly.

2. Review the template to ensure you are passing the all the parameters correctly.
    * See [some samples](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates#template-for-a-more-advanced-static-threshold-metric-alert) for metric alert templates.

3. If you are receiving a `Metric  not found` error, ensure you are using the Metric name from [this page](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported) and not the Metric Display Name

4. If you are creating [metric alerts on logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs), ensure appropriate dependencies are included.
    * See [sample template](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#resource-template-for-metric-alerts-for-logs).

5. Review if you have appropriate permissions. To create/update/delete metric alerts
    * you should have been assigned built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or
    * you should have been [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/metricAlerts

## **Recommended Documents**

[How metric alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)<br>
[Metric alerts template reference](https://docs.microsoft.com/azure/templates/microsoft.insights/2018-03-01/metricalerts)