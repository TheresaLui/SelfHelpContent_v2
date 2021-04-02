<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="No data is found for the specified time range"
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-missing-ingestion-data"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32602225"
resourceTags=""
productPesIds="15693"
cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Where's my data?

## **No data found in the time range**
<!--issueDescription-->
Our diagnostic has detected that the configured application(s) have not sent any data to the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> <!--$Time-->[Time]<!--/$Time-->. This is an indication that there is a configuration issue with your application and you should follow the troubleshooting steps below to correct your issue.
<!--/issueDescription-->

## **Recommended Steps**

If you've configured your application to send data to Application Insights, but aren't seeing the data you expect, try the following steps:

1. If you *aren't seeing any data at all*, validate that your instrumentation key is set correctly through your code or in your configuration file
2. If you *used to see data but don't anymore*, validate that a deployment has not modified or removed Application Insights configuration or dependencies. If you have configured your application to send data through Status Monitor and web published, ensure you do not select the "delete existing files" option during publish.
3. If you *see data for a pre-production/development environment but not your production environment*, ensure that you have [configured your firewall to allow traffic through the ports required](https://docs.microsoft.com/azure/application-insights/app-insights-ip-addresses) for Application Insights to send data. In addition, if your instrumentation key is set programmatically or through a configuration file, validate that these values are correct.

If none of these steps resolve your issue, review checklists in the links below for the SDK or method of application instrumentation you are using.

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)<br>
* [Troubleshoot issues seeing data with Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [using the 2.x SDK without the Java 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)<br>
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)<br>
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
