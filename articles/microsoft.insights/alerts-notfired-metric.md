<properties
	pageTitle="A metric alert should have fired but I don't see it in the Azure portal"
	description="A metric alert should have fired but I don't see it in the Azure portal"
	infoBubbleText=""
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-notfired-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32739794"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# A metric alert should have fired but I don't see it in the Azure Portal

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you think that your metric alert should have triggered but it did not, use the following steps.

1. Review the alert rule configuration:

    - Check that the **Aggregation type** and **Aggregation granularity (period)** are configured as expected. **Aggregation type** determines how metric values are aggregated (learn more [here](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-aggregation-explained#aggregation-types)), and **Aggregation granularity (period)** controls how far back the evaluation aggregates the metric values each time the alert rule runs.
    - Check that the **Threshold value** or **Sensitivity** are configured as expected.
    - Review the Dynamic Thresholds advanced settings, if used, because **Number of violations** may filter alerts and **Ignore data before** can impact how the thresholds are calculated.

Edit the rule to match what you want.

**Note:** Dynamic Thresholds requires at least 3 days of data before becoming active and chart will display continuous historical thresholds, which include thresholds updates over time.

2. Review the [fired alerts list](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see if there are any alerts fired for your metric alert rule. If you can see the alert in the portal, then the issue might be with notifications:

    - Check if proper actions/notifications were configured for the alert rule using an associated [action group](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups) or an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)
    - Check if you have any rules that might prevent receiving emails from [Azure emails](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information)
    - Check if your web hook receiver accepts the [payload sent by metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time#payload-schema)
    - Check if you have any [action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) that suppress notifications for your alert rule

3. Check if the monitor condition of the alert is fired/activated. Metric alerts are stateful, meaning that once an alert is fired on a specific metric time series, additional alerts on that time series will not be fired until the issue is no longer observed. This is done to reduce noise in case of flapping conditions. The alert rule will automatically get resolved/deactivated when the alert condition is not met for three consecutive periods.<br/><br/>If you want to make a specific metric alert rule stateless, and get alerted on every evaluation in which the alert condition is met, you will need to create the alert rule programmatically (for example, via [ARM](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-create-templates), [PowerShell](https://docs.microsoft.com/powershell/module/az.monitor/?view=azps-3.6.1), [REST](https://docs.microsoft.com/rest/api/monitor/metricalerts/createorupdate), [CLI](https://docs.microsoft.com/cli/azure/monitor/metrics/alert?view=azure-cli-latest)), and set the `autoMitigate` property to `False`.

4. If you have selected some [dimension values for a metric](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#using-dimensions), the alert will monitor each individual metric time-series (as defined by a combination of dimension values) for breaching the threshold. If you would like to also monitor the aggregate metric time-series (without any dimensions selected), then configure an additional alert rule on the metric without selecting dimensions.

5. If you are visualizing the metric condition using [Metrics chart](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/metrics), ensure that:

    - The **Aggregation** in the metric chart is the same as **Aggregation type** in your alert rule
    - The **Time granularity** is set to be same as the **Aggregation granularity (period)** in your alert rule and not set to automatic

6. If this is a [metric alert rule for logs](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs), make sure that a corresponding ScheduledQueryRule, which converts the logs data into metrics, also exists in your environment. When creating a metric alert rule for logs via the Azure Portal, the corresponding ScheduledQueryRule is created automatically, but if the metric alert rule was created programmatically, there's need to manually create the ScheduledQueryRule. [Learn more](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-logs#resource-template-for-metric-alerts-for-logs) about how to create the ScheduledQueryRule via an Azure Resource Manager template.

## **Recommended Documents**

- [How to view/edit metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)
- [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
- [Learn more about Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)
- [Learn more about the typical latency for metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#typical-latency)
