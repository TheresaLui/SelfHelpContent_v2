<properties 
    pageTitle="Server Dependencies data is incorrect or missing on Performance screen"
    description="Troubleshooting guide for missing/incorrect dependencies in the Performance triage experience"
    service="microsoft.insights"
    resource="components"
    authors="sdash"
    ms.author="sdash"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729626"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	articleId="insights-serverdependenciesmissing-performance"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Server Dependencies data is incorrect or missing on Performance screen

Dependencies are grouped by the "name" attribute in the Performance & Failure triage experiences. Dependency name is typically a low cardinality value representing the command initiated by that dependency call, such as the stored procedure name for SQL, or the URL path template for HTTP.  

## **Recommended Steps**

If you do not see a Dependency, try the following steps:

1. The dependency you are looking for may not have been called in the selected time period. Try using a longer time range.
2. Is the dependency type you are looking for, in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies)? If not, has your application been instrumented with [TrackDependency](https://docs.microsoft.com/en-us/azure/azure-monitor/app/api-custom-events-metrics#trackdependency) to collect calls to it?
3. If you aren't seeing any data at all, validate that your instrumentation key is set correctly through your code or in your configuration file. 
4. Ensure the Server/Browser toggle, is set to Server.
5. Check for any other filters on the page. A filter on roles may be excluding the role which executed the dependency call you are looking for. Try resetting the filters.
6. Go to Logs (resource menu option, or with "View in Logs" at the top), and run the following query, with an appropriate time period:

~~~kusto
    dependencies
    | where timestamp > ago(1h) 
    | summarize count() by name, target, type, data, cloud_RoleName
~~~

7. If you see the expected dependency in the results of this query, with an incorrect name: Use a [custom Telemetry initializer](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#addmodify-properties-itelemetryinitializer) to override the dependency name to an appropriate meaningful value.  

8. If you do not see the expected dependency, check to see if that dependency type is in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies)? If not, has your application been instrumented with [TrackDependency](https://docs.microsoft.com/en-us/azure/azure-monitor/app/api-custom-events-metrics#trackdependency) to collect calls to it? 
9. Check to see if sampling is in effect. You can use the following Logs query to see the actual sampling rate per type of telemetry item:

~~~kusto
union requests,dependencies,pageViews,browserTimings,exceptions,traces
| where timestamp > ago(1d)
| summarize RetainedPercentage = 100/avg(itemCount) by bin(timestamp, 1h), itemType
~~~

If you see that `RetainedPercentage` for requests is less than `100`, then a request that is rarely called (and the dependencies called in its processing) may have been sampled out. Dependencies are sampled in, only when the related request is sampled in. See [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling) to configure sampling from your code for the specific SDK implementation you are using and the kind of sampling you wish to configure.

## **Recommended Documents**
* [Dependency data model](https://docs.microsoft.com/azure/azure-monitor/app/data-model-dependency-telemetry)<br>
* [Diagnosing performance issues with Application Insights](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-performance)<br>
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
