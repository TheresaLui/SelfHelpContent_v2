<properties
    pageTitle="I can't find my resource to select it in metrics explorer"
    description="I can't find my resource to select it in metrics explorer"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="metrics-chart-shows-no-data"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public,fairfax"
/>

# My chart shows no data

Sometimes the charts in metrics explorer might show no data after selecting correct resources and metrics. This behavior can be caused by several of the following reasons:

## Microsoft.Insights resource provider isn't registered for your subscription

Exploring metrics requires *Microsoft.Insights* resource provider registered in your subscription. In many cases, it is registered automatically (that is, after you configure an alert rule, customize diagnostic settings for any resource, or configure an autoscale rule). If the Microsoft.Insights resource provider is not registered, you must manually register it by following steps described in [Azure resource providers and types](../../azure-resource-manager/resource-manager-supported-services.md).

**Solution:** Open **Subscriptions**, **Resource providers** tab, and verify that *Microsoft.Insights* is registered for your subscription.

## You don't have sufficient access rights to your resource

In Azure, access to metrics is controlled by [role-based access control (RBAC)](../../role-based-access-control/overview.md). You must be a member of [monitoring reader](../../role-based-access-control/built-in-roles.md#monitoring-reader), [monitoring contributor](../../role-based-access-control/built-in-roles.md#monitoring-contributor), or [contributor](../../role-based-access-control/built-in-roles.md#contributor) to explore metrics for any resource.

**Solution:** Ensure that you have sufficient permissions for the resource from which you are exploring metrics.

## Your resource didn't emit metrics during the selected time range

Some resources don’t constantly emit their metrics. For example, Azure will not collect metrics for stopped virtual machines. Other resources might emit their metrics only when some condition occurs. For example, a metric showing processing time of a transaction requires at least one transaction. If there were no transactions in the selected time range, the chart will naturally be empty. Additionally, while most of the metrics in Azure are collected every minute, there are some that are collected less frequently. See the metric documentation to get more details about the metric that you are trying to explore.

**Solution:** Change the time of the chart to a wider range. You may start from “Last 30 days” using a larger time granularity (or relying on the “Automatic time granularity” option).

## You picked a time range greater than 30 days

[Most metrics in Azure are stored for 93 days](data-platform-metrics.md#retention-of-metrics). However, you can only query for no more than 30 days worth of data on any single chart. This limitation doesn't apply to [log-based metrics](../app/pre-aggregated-metrics-log-metrics.md#log-based-metrics).

**Solution:** If you see a blank chart or your chart only displays part of metric data, verify that the difference between start- and end- dates in the time picker doesn't exceed the 30-day interval.

## All metric values were outside of the locked y-axis range

By [locking the boundaries of chart y-axis](metrics-charts.md#lock-boundaries-of-chart-y-axis), you can unintentionally  make the chart display area not show the chart line. For example, if the y-axis is locked to a range between 0% and 50%, and the metric has a constant value of 100%, the line is always rendered outside of the visible area, making the chart appear blank.

**Solution:** Verify that the y-axis boundaries of the chart aren’t locked outside of the range of the metric values. If the y-axis boundaries are locked, you may want to temporarily reset them to ensure that the metric values don’t fall outside of the chart range. Locking the y-axis range isn’t recommended with automatic granularity for the charts with **sum**, **min**, and **max** aggregation because their values will change with granularity by resizing browser window or going from one screen resolution to another. Switching granularity may leave the display area of your chart empty.

## You are looking at a Guest OS metric but didn’t enable Azure Diagnostic Extension

Collection of **Guest OS** metrics requires configuring the Azure Diagnostics Extension or enabling it using the **Diagnostic Settings** panel for your resource.

**Solution:** If Azure Diagnostics Extension is enabled but you are still unable to see your metrics, follow steps outlined in [Azure Diagnostics Extension troubleshooting guide](diagnostics-extension-troubleshooting.md#metric-data-doesnt-appear-in-the-azure-portal). See also the troubleshooting steps for [Cannot pick Guest OS namespace and metrics](metrics-troubleshoot.md#cannot-pick-guest-os-namespace-and-metrics)

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
