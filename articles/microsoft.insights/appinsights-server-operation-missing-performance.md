<properties 
    pageTitle="Server Operations data is incorrect or missing on Performance screen"
    description="Troubleshooting guide for missing/incorrect operations in the Performance triage experience"
    service="microsoft.insights"
    resource="components"
    authors="sdash"
    ms.author="sdash"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729629"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
 	articleId="appinsights-serveroperationmissing-performance"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Server Operations data is incorrect or missing on Performance screen

Operations help with grouping similar requests. Application Insights SDKs set the Operation name attribute in the telemetry, which is used to group requests to triage server side performance issues with related dependencies. 

## **Recommended Steps**

If you do not see an Operation, try the following steps:

1. The operation you are looking for may not have been executed in the selected time period. Try using a longer time range.
2. If you aren't seeing any data at all, validate that your instrumentation key is set correctly through your code or in your configuration file. 
3. Ensure the Server/Browser toggle, is set to Server.
4. Check for any other filters on the page. A filter on roles may be excluding the role which executed the request you are looking for. Try resetting the filters.
5. Go to Logs (resource menu option, or with "View in Logs" at the top), and run the following query, with an appropriate time period:

~~~kusto
    requests
    | where timestamp > ago(1h) 
    | summarize count() by name, operation_Name, cloud_RoleName
~~~

6. If you see the expected request in the results of this query, with an incorrect operation name: Use a [custom Telemetry initializer](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#addmodify-properties-itelemetryinitializer) to override the operation name to an appropriate meaningful value.  

7. If you do not see the expected request, check to see if sampling is in effect (in that time period). You can use the following Logs query to see the actual sampling rate per type of telemetry item:

~~~kusto
union requests,dependencies,pageViews,browserTimings,exceptions,traces
| where timestamp > ago(1d)
| summarize RetainedPercentage = 100/avg(itemCount) by bin(timestamp, 1h), itemType
~~~

If you see that `RetainedPercentage` for requests is less than `100`, then a request rarely executed may have been sampled out. See [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling) to configure sampling from your code for the specific SDK implementation you are using and the kind of sampling you wish to configure.

## **Recommended Documents**
* [Diagnosing performance issues with Application Insights](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-performance)<br>
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
