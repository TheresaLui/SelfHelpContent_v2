<properties
	pageTitle="My metric alert fired when it shouldn't have"
	description="General troubleshooting guide for metric alert misfiring"
	infoBubbleText="Some suggestions have been found to help solve your metric alert issue more quickly."
	service="microsoft.insights"
	resource="metricalerts"
	authors="snehithm"
	ms.author="snmuvva"
	displayOrder="6"
	articleId="insights-falsealert-metric"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629644"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public, fairfax"
/>

# My metric alert fired when it shouldn't have

[Metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview) monitor platform or custom metric values for your Azure resources and notify you if a metric breaches a threshold.

## **Recommended Steps**

If you believe your metric alert shouldn't have triggered but it did, the following steps might help resolve the issue.

1. Review the [fired alerts list](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/alertsV2) to see the alert fired for your metric alert rule. Review the alert details to see the metric chart, **Metric Value** and **Threshold value** when the alert was triggered (under **Why did this alert fire?**).

**Note:** If you are using Dynamic Thresholds condition type and think that thresholds used were not correct, please provide feedback using the frown icon. This feedback will impact the machine learning algorithmic research and improve future detections.

1. If you have selected multiple dimension values for a metric, the alert will be triggered when **any** of the metric time-series (as defined by a combination of dimension values) breaches the threshold
1. Review the alert rule configuration:

    - Check that **Aggregation type**, **Aggregation granularity (period)**, and **Threshold value** or **Sensitivity** specified in the metric alert rule condition are what you want
    - Please also mind Dynamic Thresholds advanced settings, if used, as **Number of violations** may filter alerts and **Ignore data before** can impact how the thresholds are calculated.

If they are not what you want, edit the rule to match what you want.

**Note:** Dynamic Thresholds requires at least 3 days of data before becoming active and chart will display continuous historical thresholds, which include thresholds updates over time.

1. If you are visualizing the metric condition using [Metrics chart](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/metrics), ensure that:

    - **Aggregation** in the metric chart is the same as **Aggregation type** in your alert rule
    - **Time granularity** is set to be same as the **Aggregation granularity (period)** in your alert rule and not set to automatic

## **Recommended Documents**

- [How to view/edit metric alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)
- [How to view fired alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances)
- [Learn more about Dynamic Thresholds](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-dynamic-thresholds)
