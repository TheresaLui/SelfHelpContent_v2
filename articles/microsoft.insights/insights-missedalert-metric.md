<properties
	pageTitle="My metric alert doesn't fire when it should have"
	description="General troubleshooting guide for metric alert not firing"
	infoBubbleText="Some suggestions have been found to help solve your metric alert issue more quickly."
	service="microsoft.insights"
	resource="metricalerts"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="6"
	articleId="insights-missedalert-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629638"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax"
/>

# My metric alert doesn't fire when it should have

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you believe your metric alert should have triggered but it did not, the following steps might help resolve the issue.

1. Review the alert rule configuration:

    - Check that **Aggregation type**, **Aggregation granularity (period)** and **Threshold value** or **Sensitivity** specified in the metric alert rule condition are what you want
    - Please also mind Dynamic Thresholds advanced settings, if used, as **Number of violations** may filter alerts and **Ignore data before** can impact how the thresholds are calculated

If they are not what you want, edit the rule to match what you want.

**Note:** Dynamic Thresholds requires at least 3 days of data before becoming active and chart will display continuous historical thresholds, which include thresholds updates over time.

1. Review the [fired alerts list](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see if there any alerts fired for your metric alert rule. If you can see the alert in the portal, then the issue might be with notifications:

    - Check if you have any rules that might prevent receiving emails from [Azure emails](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups#action-specific-information)
    - Check if your web hook receiver accepts the [payload sent by metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-near-real-time#payload-schema)

1. If you have selected some dimension values for a metric, the alert will monitor each individual metric time-series (as defined by a combination of dimension values) for breaching the threshold. Even when metric value for the aggregate metric time-series (without any dimensions selected) breaches the threshold, the alert wouldn't fire if none of individual time-series breach the threshold.
1. If you are visualizing the metric condition using [Metrics chart](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/metrics), ensure that:

    - the **Aggregation** in the metric chart is the same as **Aggregation type** in your alert rule
    - the **Time granularity** is set to be same as the **Aggregation granularity (period)** in your alert rule and not set to automatic

## **Recommended Documents**

- [How to view/edit metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)
- [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
- [Learn more about Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)
