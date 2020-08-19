<properties 
    pageTitle="Inaccurate Application Insights metrics or gaps in metrics charts"
    description="Troubleshooting inaccurate Application Insights metrics or gaps in metrics charts"
    infoBubbleText="How to troubleshoot issues with inaccurate Application Insights metrics or gaps in the metrics charts"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    selfHelpType="generic"
    articleId="metrics-resourcespecific-appinsights-inaccurate-or-gaps"
    productPesIds="16250"
    supportTopicIds="32684758,32684759"
    cloudEnvironments="public,fairfax,mooncake,blackforest,usnat,ussec"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Troubleshooting inaccurate Application Insights metrics or gaps in metrics charts

You may see inaccurate metric charts or gaps in the Application Insights metrics in the following cases:

* Application Insights has paused collecting telemetry because the ingested volume for the day reached the [daily data cap limit](https://docs.microsoft.com/azure/azure-monitor/app/pricing#set-the-daily-cap)
* The accuracy of the log-based metric was reduced by [sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling), [filtering](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling), or [data capping](https://docs.microsoft.com/azure/azure-monitor/app/pricing#set-the-daily-cap)

There are [two types of metrics](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics) in Application Insights: **log-based metrics** and **standard pre-aggregated metrics**. The **log-based metrics** behind the scene is an abstraction layer that translates each request for metric values into a Kusto query executed on top of *raw events*. See [the underlying queries for each of the Application Insights log-based metric](https://docs.microsoft.com/azure/azure-monitor/platform/app-insights-metrics).  The telemetry volume reduction techniques such as [sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling), [filtering](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling), or [data capping](https://docs.microsoft.com/azure/azure-monitor/app/pricing#set-the-daily-cap) may reduce the volume of the collected raw events, impacting the quality of the log-based metrics.

**IMPORTANT:** If your scenario allows, always use pre-aggregated metrics instead of log-based metrics or log queries. Specifically, we recommend using them when configuring alert notifications or in the operational dashboards. Standard pre-aggregated metrics are exempt from the data cap limit and do not incur additional charges in your Azure subscription. Additionally, when metrics are pre-aggregated by the SDK, their [accuracy is not impacted by sampling](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics#pre-aggregated-metrics).

## **Recommended Steps**

1. Check the presence of the raw events for your log-based metric by manually running the [underlying Kusto Query](https://docs.microsoft.com/azure/azure-monitor/platform/app-insights-metrics) on the **Logs** tab of your Application Insights resource:
    * **When there are no events at all**, this typically indicates the misconfiguration of the SDK (or misconfiguration of the Agent in the codeless attach scenarios). In this case, verify that your application is properly onboarded and sends the data to the Application Insights resource you are looking at.
    * **A gap in the collected events** while application is running typically indicates that the ingested volume of telemetry has reached the daily data cap limit. You can verify this condition by looking an activity log event "[Application Insights component daily cap reached](https://docs.microsoft.com/azure/azure-monitor/app/pricing#create-alerts-for-the-daily-cap)".

1. Check the value of **itemCount** property on raw events. Any value greater than 1 indicates that [sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling) has reduced the volume of the collected telemetry. When this happens, each single row in the logs represents multiple occurrences of the event. Sampling may significantly impact the accuracy of the metric, especially when the [chart is using filtering](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-filters-to-charts) or [splitting by a dimension](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-splitting-to-a-chart). To improve the accuracy of the charts, you can switch to pre-aggregated metrics, or change sampling configuration to collect more raw events.

**NOTE:** you can see the effective sampling rate by running the following query in [Analytics query]( https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview):

    requests | where timestamp > ago(1d)
    | summarize 100/avg(itemCount) by bin(timestamp, 1h)
    | render areachart

## **Recommended Documents**

* [Log-based and pre-aggregated metrics in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics#pre-aggregated-metrics)
* [Underlying Kusto queries for Application Insights log-based metrics](https://docs.microsoft.com/azure/azure-monitor/platform/app-insights-metrics)
* [Manage usage and costs for Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/pricing)
* [Sending custom metrics using Application Insights SDK](https://docs.microsoft.com/azure/azure-monitor/app/pre-aggregated-metrics-log-metrics#custom-metrics-dimensions-and-pre-aggregation)
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Review the complete list of supported SDKs and platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
