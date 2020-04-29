<properties
    pageTitle="My metrics chart shows dashed line"
    description="My metrics chart shows dashed line"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="4"
    articleId="metrics-chart-shows-dashed-line"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677616"
    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-chart-shows-dashed-line -->

## My metrics chart shows dashed line

Azure metrics charts use a dashed line style to indicate a missing value (also known as "null value") between two known time grain data points. For example, if in the time selector you picked "1 minute" time granularity but the metric was reported at 07:26, 07:27, 07:29, and 07:30 (note a minute gap between second and third data points), then a dashed line will connect 07:27 and 07:29 and a solid line will connect all other data points. The dashed line drops down to zero when the metric uses count and sum aggregation. For the avg, min or max aggregations, the dashed line connects two nearest known data points. Also, when the data is missing on the rightmost or leftmost side of the chart, the dashed line expands to the direction of the missing data point.

![metric image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/missing-data-point-line-chart.png)

## **Recommended Steps**

This behavior is by design. It is useful for identifying missing data points. The line chart is a superior choice for visualizing trends of high-density metrics but may be difficult to interpret for the metrics with sparse values, especially when correlating values with time grain is important. The dashed line makes reading of these charts easier but if your chart is still unclear, consider viewing your metrics with a different chart type. For example, a scattered plot chart for the same metric clearly shows each time grain by only visualizing a dot when there is a value and skipping the data point altogether when the value is missing:

![metric image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/missing-data-point-scatter-chart.png)

**NOTE**: If you still prefer a line chart for your metric, moving mouse over the chart may help to assess the time granularity by highlighting the data point at the location of the mouse pointer.

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
