<properties
    pageTitle="My metric chart shows no data"
    description="My metric chart shows no data"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="2"
    articleId="metrics-chart-shows-no-data"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677618"
    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-chart-shows-no-data -->

Sometimes the charts in metrics explorer might show no data after selecting correct resources and metrics. This can be caused by one of the reasons listed below.

### **Microsoft.Insights resource provider isn't registered for your subscription**

Exploring metrics requires *Microsoft.Insights* resource provider registered in your subscription. In many cases, it is registered automatically (that is, after you configure an alert rule, customize diagnostic settings for any resource, or configure an autoscale rule). If the Microsoft.Insights resource provider is not registered, you must manually register it by following steps described in [Azure resource providers and types](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services).

**Recommended Steps**

* Open **Subscriptions**, **Resource providers** tab, and verify that *Microsoft.Insights* is registered for your subscription

### **You don't have sufficient access rights to your resource**

In Azure, access to metrics is controlled by [role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview). You must be a member of [monitoring reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-reader), [monitoring contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor), or [contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) to explore metrics for any resource.

**Recommended Steps**

* Ensure that you have sufficient permissions for the resource from which you are exploring metrics

### **Your resource didn't emit metrics during the selected time range**

Some resources don’t constantly emit their metrics. For example, Azure will not collect metrics for stopped virtual machines. Other resources might emit their metrics only when some condition occurs. For example, a metric showing processing time of a transaction requires at least one transaction. If there were no transactions in the selected time range, the chart will naturally be empty. Additionally, while most of the metrics in Azure are collected every minute, there are some that are collected less frequently. See the metric documentation to get more details about the metric that you are trying to explore.

**Recommended Steps**

* Change the time of the chart to a wider range. You may start from "Last 30 days" using a larger time granularity (or relying on the "Automatic time granularity" option)

### **You picked a time range greater than 30 days**

[Most metrics in Azure are stored for 93 days](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-metrics#retention-of-metrics). However, you can only query for no more than 30 days worth of data on any single chart. This limitation doesn't apply to [log-based metrics](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics#log-based-metrics).

**Recommended Steps**

* If you see a blank chart or your chart only displays part of metric data, verify that the difference between start- and end- dates in the time picker doesn't exceed the 30-day interval

### **All metric values were outside of the locked y-axis range**

By [locking the boundaries of chart y-axis](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#lock-boundaries-of-chart-y-axis), you can unintentionally  make the chart display area not show the chart line. For example, if the y-axis is locked to a range between 0% and 50%, and the metric has a constant value of 100%, the line is always rendered outside of the visible area, making the chart appear blank.

**Recommended Steps**

* Verify that the y-axis boundaries of the chart aren’t locked outside of the range of the metric values. If the y-axis boundaries are locked, you may want to temporarily reset them to ensure that the metric values don’t fall outside of the chart range. Locking the y-axis range isn’t recommended with automatic granularity for the charts with **sum**, **min**, and **max** aggregation because their values will change with granularity by resizing browser window or going from one screen resolution to another. Switching granularity may leave the display area of your chart empty.

### **You are looking at a VM Guest OS metric (for example, "Available memory") but didn’t enable Azure Diagnostic Extension**

Collection of **Guest OS** metrics requires configuring the Azure Diagnostics Extension or enabling it using the **Diagnostic Settings** panel for your resource.

**Recommended Steps**

* If Azure Diagnostics Extension is enabled but you are still unable to see your metrics, follow steps outlined in [Azure Diagnostics Extension troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-troubleshooting#metric-data-doesnt-appear-in-the-azure-portal). See also the troubleshooting steps for [Cannot pick Guest OS namespace and metrics](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot#cannot-pick-guest-os-namespace-and-metrics).

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
