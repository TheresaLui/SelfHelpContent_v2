<properties 
    pageTitle="Tetris Self Help Doc Placeholder"
    description="Tetris Doc Placeholder"
    service="microsoft.insights"
    resource="components"
    authors="neilghuman"
    ms.author="neghuman"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32780459"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
 	articleId="appinsights-tetris-self-help-doc-placeholder"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Server Operations data is incorrect or missing on Failures screen

Operations help with grouping similar requests. Application Insights SDKs set the Operation name attribute in the telemetry, which is used to group requests to triage server side failures with related exceptions or dependency failures. 

## **Recommended Steps**

If you do not see a failed Operation, try the following steps:

1. The operation you are looking for may not have been executed, or may not have failed in the selected time period. Try using a longer time range.
2. If you aren't seeing any data at all, validate that your instrumentation key is set correctly through your code or in your configuration file. 
3. Ensure the Server/Browser toggle, is set to Server.
4. Check for any other filters on the page. A filter on roles may be excluding the role which executed the request you are looking for. Try resetting the filters.


## **Recommended Documents**
* [Diagnosing failures with Application Insights](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-runtime-exceptions)
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
