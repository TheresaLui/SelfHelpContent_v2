<properties
	pageTitle="My metric alert doesn't fire when it should have"
	description="General troubleshooting guide for metric alert not firing"
	infoBubbleText="Some suggestions have been found to help solve your metric alert issue more quickly."
	service="microsoft.insights"
	resource="metricalerts"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="6"
	articleId="insights-missedalert-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629638"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# My metric alert doesn't fire when it should have

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you believe your metric alert should have triggered but it did not, the following steps might help resolve the issue.

1. Review the alert rule configuration:

    - Check that **Aggregation type**, **Aggregation granularity (period)** and **Threshold value** or **Sensitivity** specified in the metric alert rule condition are what you want
    - Please also mind the Dynamic Thresholds advanced settings, if used, as **Number of violations** may filter alerts and **Ignore data before** can impact how the thresholds are calculated

If they are not what you want, edit the rule to match what you want.

**Note:** Dynamic Thresholds requires at least 3 days of data before becoming active and chart will display continuous historical thresholds, which include thresholds updates over time.

2. Review the [fired alerts list](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see if there any alerts fired for your metric alert rule. If you can see the alert in the portal, then the issue might be with notifications:

    - Check if proper actions/notifications were configured for the alert rule using an associated [action group](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups) or an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)
    - Check if you have any rules that might prevent receiving emails from [Azure emails](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information)
    - Check if your web hook receiver accepts the [payload sent by metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time#payload-schema)
    - Check if you have any [action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) that suppress notifications for your alert rule

3. Check if the monitor condition of the alert is fired/activated. Metric alerts are stateful, meaning that once an alert is fired on a specific metric time series, additional alerts on that time series will not be fired until the issue is no longer observed. This is done to reduce noise in case of flapping conditions. The alert rule will automatically get resolved/deactivated when the alert condition is not met for three consecutive periods.<br/><br/>If you wish to make a specific metric alert rule stateless, and get alerted on every evaluation in which the alert condition is met, you will need to create the alert rule programmatically (e.g. via ARM, PowerShell, REST, CLI), and set the *autoMitigate* property to 'False'.

4. If you have selected some [dimension values for a metric](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#using-dimensions), the alert will monitor each individual metric time-series (as defined by a combination of dimension values) for breaching the threshold. If you would like to also monitor the aggregate metric time-series (without any dimensions selected), then configure an additional alert rule on the metric without selecting dimensions.

5. If you are visualizing the metric condition using [Metrics chart](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/metrics), ensure that:

    - The **Aggregation** in the metric chart is the same as **Aggregation type** in your alert rule
    - The **Time granularity** is set to be same as the **Aggregation granularity (period)** in your alert rule and not set to automatic

## **Recommended Documents**

- [How to view/edit metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)
- [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
- [Learn more about Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)
- [Learn more about the typical latency for metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview#typical-latency)
