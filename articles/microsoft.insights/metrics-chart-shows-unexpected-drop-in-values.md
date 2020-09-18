<properties
    pageTitle="My chart shows unexpected drop in values"
    description="My chart shows unexpected drop in values"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="5"
    articleId="metrics-chart-shows-unexpected-drop-in-values"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677619"
    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-chart-shows-unexpected-drop-in-values -->

## My chart shows unexpected drop in values

In many cases, the perceived drop in the metric values is a misunderstanding of the data shown on the chart. You can be misled by a drop in sums or counts when the chart shows the most-recent minutes because the last metric data points haven’t been received or processed by Azure yet. Depending on the service, the latency of processing metrics can be within a couple minutes range. For charts showing a recent time range with a 1- or 5- minute granularity, a drop of the value over the last few minutes becomes more noticeable:

![metric image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/drop-in-values.png)

## **Recommended Steps**

This behavior is by design. We believe that showing data as soon as we receive it is beneficial even when the data is *partial* or *incomplete*. Doing so allows you to make important conclusion sooner and start investigation right away. For example, for a metric that shows the number of failures, seeing a partial value X tells you that there were at least X failures on a given minute. You can start investigating the problem right away, rather than wait to see the exact count of failures that happened on this minute, which might not be as important. The chart will update once we receive the entire set of data, but at that time it may also show new incomplete data points from more recent minutes.

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
