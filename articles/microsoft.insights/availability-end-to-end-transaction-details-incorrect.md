<properties 
    pageTitle="I am seeing incomplete data on my Availability tests"
    description="I am seeing incomplete data on my Availability tests"
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "casocha"
    articleId="availability-end-to-end-transaction-details-incorrect"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
    productPesIds="15693"
    supportTopicIds="32729582"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# I can see end-to-end Availability test details, but I'm seeing incomplete or no data

Selecting a web test result on a scatter plot or in search fails to show any correlating server-side telemetry (e.g., requests, custom events, traces, dependencies). The web test result shows the **E2E Transaction Details** view and individual steps for the web test.

![Telemetry image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/end2endpic1.jpg)

## **Recommended Steps**

**I'm not seeing any data**<br>
* Validate that your instrumentation key is set correctly through your code or in your configuration file

**Data is coming through but doesn't match what I expect**<br>
* [Double check your sampling settings](https://docs.microsoft.com/azure/azure-monitor/app/sampling). By default, adaptive sampling generally only occurs at higher traffic volumes.

**I used to see data, but don't anymore**<br>
* Check that a deployment has not modified or removed Application Insights configuration or dependencies
* If you configured your application to send data through Status Monitor and web published, ensure you don't select the **delete existing files** option during publish

**I see data in my pre-production/development environment, but not in production**<br>
* Check that you've configured your firewall to allow traffic through the ports required for Application Insights to send data
* If your instrumentation key is set programmatically or through a configuration file, validate that these values are correct

If none of these steps resolve your issue, see additional checklists in the next section for the SDK or method of application instrumentation you use.

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [using the 2.x SDK without the Java 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)
