<properties
	pageTitle="Alert issues with Managed Instance"
	description="Alert issues with Managed Instance"
	infoBubbleText="Alert issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748860"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-monitoring-alerts.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Alert issues with Managed Instance

[Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-overview) are generated when an import condition, such as storage size or CPU usage, reach a defined threshold.  An alert can notify you (e.g, send an email, call, text message) or trigger actions such as a [web hook](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks), run Azure Functions, etc.

Alerting metrics are only available for the managed instance, not individual databases.  Database diagnostics telemetry is available in the form of [diagnostics logs](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure#diagnostic-telemetry-for-export). Alerts on diagnostics logs can be set up from within [SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql) using [log alert scripts](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-sql-managed-instance).

New alert rule will become active within a few minutes and you can only access alerts generated in the **last 30 days**.
For metric alerts, typically you will get notified in under 5 minutes if you set the alert rule frequency to be 1 min. In cases of heavy load for notification systems, you might see a longer latency.

The consumption and [management](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal) of alert instances requires the user to have the Azure built-in roles of either [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor) or [monitoring reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader). These roles are supported at any Azure Resource Manager scope, from the subscription level to granular assignments at a resource level.

### Can’t create alerts using Azure Portal
- Confirm your resource name does not contain special characters
- Try using [REST API](https://docs.microsoft.com/rest/api/monitor/alertrules), [CLI](https://docs.microsoft.com/cli/azure/monitor/alert?view=azure-cli-latest) ([Samples](https://docs.microsoft.com/azure/azure-monitor/samples/cli-samples#work-with-alerts)) or Powershell ([add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2?view=azps-4.6.1), [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2?view=azps-4.6.1), [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria?view=azps-4.6.1), [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection?view=azps-4.6.1) and [Remove-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/remove-azmetricalertrulev2?view=azps-4.6.1))

### Receiving too many alerts
- Confirm if the threshold value used is not too low for your workload 
- If the aggregation type is configured to "Maximum" try changing to "Average" of the alert
- Try increasing the "Frequency of evaluation" of the alert

Alerts can be [suppressed](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules?tabs=portal#suppression-of-alerts), for example for a planned maintenance window from **Now (Always)**, **At a scheduled time** and **With a recurrence**.

## **Recommended Steps**

### Set Up Alerts for SQL Managed Instance
- To configure alerts for SQL Managed Instance, see [Create Alert for SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create?WT.mc_id=Portal-Microsoft_Azure_Support)


## **Recommended Documents**
* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal)
* [Understand how metric alerts work in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
