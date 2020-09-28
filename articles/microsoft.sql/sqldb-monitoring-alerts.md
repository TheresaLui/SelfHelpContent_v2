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
	articleId="sqlmi-monitoring-alerts.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Alert issues with Azure SQL Database

[Alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-overview) can be configured on metric values for SQL Managed Instance. Alerts can send you an email, call a web hook, run Azure Functions, runbook, call an external ITSM compatible ticketing system, call you on the phone or send a text message when some metric, for example instance storage size or CPU usage, reaches a predefined threshold. Alerts proactively notify you when important conditions are found in your monitoring data. They allow you to identify and address issues before the users of your system notice them.

Alerting metrics are available for managed instance **only**. Alerting metrics for individual databases in managed instance are **not available**. Database diagnostics telemetry is on the other hand available in the form of [diagnostics logs](https://docs.microsoft.com/azure/azure-sql/database/metrics-diagnostic-telemetry-logging-streaming-export-configure#diagnostic-telemetry-for-export). Alerts on diagnostics logs can be setup from within [SQL Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql) product using [log alert scripts](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql#creating-alerts-for-sql-managed-instance) for managed instance.

New alert rule will become active within a few minutes and you can only access alerts generated in the **last 30 days**.
For metric alerts, typically you will get notified in under 5 minutes if you set the alert rule frequency to be 1 min. In cases of heavy load for notification systems, you might see a longer latency.

Alerts can be [suppressed](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules?tabs=portal#suppression-of-alerts) for example for a planned maintenance window. Alerts can be suppressed From __Now(Always)__, __At a scheduled time__ and __With a recurrence__.

Existing alerts need to be managed from Alerts menu from Azure portal dashboard. Existing alerts **cannot be modified** from Managed Instance resource blade.
•	Search for “Alerts” using Azure portal Search
•	Click on “[Monitor](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade)” on the navigation bar then select “[Alerts](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2)” 
•	Click on “[Alerts](https://ms.portal.azure.com/#blade/Microsoft_Azure_Monitoring/AlertsManagementSummaryBlade)” on the Azure navigation bar, if you have it configured.

The consumption and management of alert instances requires the user to have the Azure built-in roles of either [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor) or [monitoring reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader). These roles are supported at any Azure Resource Manager scope, from the subscription level to granular assignments at a resource level.

### Can’t create alerts using Azure Portal
- Confirm if your resource is not using special characters in the name
- Try using REST API, CLI or Powershell

### Receiving too many alerts
- Confirm if the threshold value used is not too low for your workload 
- If the aggregation type is configured to "Maximum" try changing to "Average" of the alert
- Try increasing the "Frequency of evaluation" of the alert

## **Recommended Steps**

### Set Up Alerts for SQL Managed Instance
- To configure alerts for SQL Managed Instance, see [Create Alert for SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create?WT.mc_id=Portal-Microsoft_Azure_Support)

### Build Your Own Solution Using DMV Querying
- Schedule your own queries using the built-in agent
- Use the database mail feature in SQL Managed Instance to send email notifications automatically upon the DMV query result. Note that database administrator knowledge is required for this option.

### Use a Third-Party Product that Supports SQL Managed Instance
- Consider using a third-party tool that supports SQL Managed Instance for your monitoring requirements


## **Recommended Documents**
* [Create, view and manage classic metric alerts using Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-classic-portal)
* [Azure CLI](https://docs.microsoft.com/cli/azure/monitor/alert?view=azure-cli-latest) only for classic metric alerts ([Samples](https://docs.microsoft.com/azure/azure-monitor/samples/cli-samples#work-with-alerts))
* [Azure Monitor REST API](https://docs.microsoft.com/rest/api/monitor/alertrules)
* Powershell [add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2?view=azps-4.6.1), [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2?view=azps-4.6.1), [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria?view=azps-4.6.1), [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection?view=azps-4.6.1) and [Remove-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/remove-azmetricalertrulev2?view=azps-4.6.1)
* [Create activity log alerts on service notifications](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal)
* [Understand how metric alerts work in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
* [Call a webhook with a classic metric alert in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-webhooks)
* [Monitoring Microsoft Azure SQL Database and Azure SQL Managed Instance performance using dynamic management views](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs?WT.mc_id=Portal-Microsoft_Azure_Support#monitor-resource-use)
* [Configure Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/configure-database-mail?WT.mc_id=Portal-Microsoft_Azure_Support&view=sql-server-ver15)
