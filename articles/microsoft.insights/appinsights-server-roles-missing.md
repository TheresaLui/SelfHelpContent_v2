<properties 
    pageTitle="Server Roles are incorrect or missing on Performance/Failures screen"
    description="Troubleshooting guide for missing/incorrect roles in the Performance/Failures triage experiences"
    service="microsoft.insights"
    resource="components"
    authors="sdash"
    ms.author="sdash"
    displayOrder="1"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729630,32729631"
    cloudEnvironments="public, Fairfax, mooncake, usnat, ussec"
 	articleId="appinsights-serverrolesmissing"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Server Roles are incorrect or missing on Performance/Failures screen

Server roles are used to logically group the components/application processes. The Application Insights SDK tries to automatically set a meaningful value for the cloud role name property. For example, when you’re running in Azure App Service, the name of the web app is used.

## **Recommended Steps**

If you do not see a Role, try the following steps:

1. If your application components are running in environments such as IaaS/On-premises VMs, the SDK does not set a value for the `Cloud_RoleName` property. That would result in all of the data to be aggregated under a single role called `<no role name>`. On the Application Map experience, this group is called the same name as the Application Insights resource. Use a [custom Telemetry initializer](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#addmodify-properties-itelemetryinitializer) to [override the cloud role name](https://docs.microsoft.com/azure/azure-monitor/app/app-map?tabs=net#set-cloud-role-name) to an appropriate meaningful value for each distinct component of your distributed application.
2. Check for any other filters on the page. A filter on roles may be excluding the role you are looking for. Try resetting the filters.
3. Try using a different time period, if the role you are looking for may not have processed calls recently.
4. If you are seeing no data, validate that your instrumentation key is set correctly through your code or in your configuration file.

## **Recommended Documents**
* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [using the 2.x SDK without the 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
