<properties 
    pageTitle="Server Exceptions data is incorrect or missing on Failures screen"
    description="Troubleshooting guide for missing/incorrect exceptions in the Failures triage experience"
    service="microsoft.insights"
    resource="components"
    authors="sdash"
    ms.author="sdash"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729627"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
 	articleId="appinsights-serverexceptionsmissing-failures"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Server Exceptions data is incorrect or missing on Failures screen

Exceptions represent a handled or unhandled exception that occurred during execution of the monitored application. In the Failures experience, exceptions are grouped by `Problem Id`, which is typically a combination of exception type and function from the call stack.

## **Recommended Steps**

If you do not see an exception, try the following steps:

1. Are you looking for a handled exception? While unhandled exceptions are auto-collected, handled exceptions need to be explicitly reported using the [TrackException SDK](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-exceptions#reporting-exceptions-explicitly).
2. Some exceptions like the following cannot be collected automatically. They will need to be explicitly reported using the [TrackException SDK](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-exceptions#reporting-exceptions-explicitly).
    * Exceptions thrown from controller constructors.
    * Exceptions thrown from message handlers.
    * Exceptions thrown during routing.
    * Exceptions thrown during response content serialization.
    * Exception thrown during application start-up.
    * Exception thrown in background tasks.

2. If you are using MVC 4 (and prior), or a very old Application Insights Web SDK, version 2.5 (and prior): then the unhandled exceptions are only collected if the CustomErrors configuration is set to `Off`. If it is set to `On`, then follow the [guidance](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-exceptions#prior-versions-support) to collect exceptions.
2. If it is a WCF application, see [this](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-exceptions#wcf) to collect exceptions.
3. If you aren't seeing any data at all, validate that your instrumentation key is set correctly through your code or in your configuration file.
4. Ensure the Server/Browser toggle, is set to Server.
5. Check for any other filters on the page. A filter on roles may be excluding the exception you are looking for. Try resetting the filters.
6. Check to see if sampling is in effect. You can use the following Logs query to see the actual sampling rate per type of telemetry item:

~~~kusto
union requests,dependencies,pageViews,browserTimings,exceptions,traces
| where timestamp > ago(1d)
| summarize RetainedPercentage = 100/avg(itemCount) by bin(timestamp, 1h), itemType
~~~

If you see that `RetainedPercentage` for requests is less than `100`, then a rare request failure may have been sampled out. Exceptions are sampled in, only when the related request is sampled in. See [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling) to configure sampling from your code for the specific SDK implementation you are using and the kind of sampling you wish to configure.

## Duplicate exceptions

Starting with Application Insights Web SDK version 2.6 (beta3 and later), Application Insights collects unhandled exceptions thrown in the MVC 5+ and WebAPI 2+ controllers methods automatically. If you have previously added a custom handler to track such exceptions, please remove them to prevent double tracking of exceptions.

## **Recommended Documents**
* [Diagnosing failures with Application Insights](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-runtime-exceptions)<br>
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
