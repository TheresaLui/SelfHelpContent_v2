<properties
	pageTitle="Alert issues with Azure SQL Database"
	description="Alert issues with Azure SQL Database"
	infoBubbleText="Alert issues with Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749523"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqldb-monitoring-alerts.md"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve Alert issues with Azure SQL Database

Most users can resolve alert issues with Azure SQL Database by following the information below.

[Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-overview) are generated when an import condition, such as storage size or CPU usage, reaches a defined threshold. An alert can notify you (for exmple, can call you, or send an email message or a text message) or trigger actions, such as calling a [web hook](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks), running Azure Functions, and so on.

Database diagnostics telemetry is available in the form of [diagnostics logs](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure#diagnostic-telemetry-for-export). Alerts on diagnostics logs can be set up from within [SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql) by using [log alert scripts](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-azure-sql-database).

The consumption and [management](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal) of alert instances requires the user to have the Azure built-in roles of either [Monitoring Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor) or [Monitoring Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader). These roles are supported at any Azure Resource Manager scope, from the subscription level to granular assignments at a resource level.

## **Recommended Steps**

### Can’t create alerts using Azure Portal
- Confirm that your resource name does not contain special characters
- Try using [REST API](https://docs.microsoft.com/rest/api/monitor/alertrules), [CLI](https://docs.microsoft.com/cli/azure/monitor/alert?view=azure-cli-latest) ([Samples](https://docs.microsoft.com/azure/azure-monitor/samples/cli-samples#work-with-alerts)) or PowerShell ([add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2?view=azps-4.6.1), [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2?view=azps-4.6.1), [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria?view=azps-4.6.1), [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection?view=azps-4.6.1) and [Remove-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/remove-azmetricalertrulev2?view=azps-4.6.1))

### Receiving too many alerts
- Confirm if the threshold value used is not too low for your workload 
- If the aggregation type is configured to "Maximum," try changing it to "Average" in the alert
- Try increasing the "Frequency of evaluation" of the alert

Alerts can be [suppressed](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules?tabs=portal#suppression-of-alerts). For example, for a planned maintenance window, you can suppress alerts with the specifications of **Now (Always)**, **At a scheduled time**, and **With a recurrence**.

### Set up alerts for a SQL Managed Instance
- To configure alerts for Azure SQL Database, see [Create alerts for Azure SQL Database and Azure Synapse Analytics by using the Azure Portal](https://docs.microsoft.com/azure/azure-sql/database/alerts-insights-configure-portal)

## **Recommended Documents**
* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal)
* [Understand how metric alerts work in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
