<properties 
    pageTitle="Troubleshooting Metrics Explorer"
    description="Troubleshooting Metrics Explorer"
    infoBubbleText="Here are some things to help with your metric explorer issues"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    ms.author="mcosner"
    selfHelpType="generic"
    articleId="appinsights-metricsexplorer"
    productPesIds="15693"
    supportTopicIds="32602208"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Metrics Explorer

## **Recommended Steps**

**No Data/Blank Charts**<br>

Often, you may select an incorrect time range or metric - for example, you might select an App Service resource by mistake. Please follow these steps to verify you have data for your Application Insights resource.

1. Please verify that the **Application Insight** resource is selected
2. Please review all parameters for your [filters](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-filters-to-charts) ensuring the Time Range and Metric are correct (too small of a time range may not show data)
3. Ensure you did not [pin the chart axis](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#lock-boundaries-of-chart-y-axis) to a value that is out of range
4. Validate that the data is being sent to Application Insights by running an [analytics query](https://docs.microsoft.com/azure/azure-monitor/app/analytics)

**Incorrect Data/Values**<br>

When data does not look correct in the chart, it is usually due to the amount of data sent by the application, or the time range and granularity. Please follow these steps to verify the data for your Application Insights resource is correct.

1. Please verify that the **Application Insight** resource is selected
2. Please review all parameters for your [filters](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-filters-to-charts) ensuring the Time Range and Metric are correct (too small of a time range may not show data)
3. Validate that the data is being sent to Application Insights by running an [analytics query](https://docs.microsoft.com/azure/azure-monitor/app/analytics)
4. If your values look too small, check to make sure that the values are being auto scaled (bytes to Megabytes for example)
5. If you only see **some** of your data, you may have [sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling) enabled
6. In addition to the previous item, your **Time Range** will automatically set the aggregation time, the bigger the range the more items are aggregated

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting issues with metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
