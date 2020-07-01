<properties
    pageTitle="My chart shows Error Retrieving Data message on dashboard"
    description="My chart shows Error Retrieving Data message on dashboard"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="3"
    articleId="metrics-error-retrieving-data-message-on-dashboard"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677617"
    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-error-retrieving-data-message-on-dashboard -->

## My chart shows Error Retrieving Data message on dashboard

This problem may happen when your dashboard was created with a metric that was later deprecated and removed from Azure. To verify that it is the case, open the **Metrics** tab of your resource, and check the available metrics in the metric picker. If the metric is not shown, the metric has been removed from Azure. Usually, when a metric is deprecated, there is a better new metric that provides with a similar perspective on the resource health.

## **Recommended Steps**

Update the failing tile by picking an alternative metric for your chart on dashboard. You can [review a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported).

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
