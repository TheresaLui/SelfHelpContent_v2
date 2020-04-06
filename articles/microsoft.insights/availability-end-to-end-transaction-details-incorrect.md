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
    cloudEnvironments="public, Fairfax"
    productPesIds="15693"
    supportTopicIds="32729582"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# I can see the end to end Availability test details but I'm seeing incomplete or no data

You click on a web test result (either on the scatter plot or via search) to drill down and learn more details of the call. You can see the E2E Transaction Details view and the individual steps for the web test pinging your site, but you don’t see any correlated server-side telemetry (e.g. requests, custom events, traces, exceptions).

![telemetry image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/end2endpic1.jpg)

## **Recommended Steps**

### I'm not seeing any data

* Validate that your instrumentation key is set correctly through your code or in your configuration file.

### Data is coming through but doesn't match what I expect

* [Double check your sampling settings](https://docs.microsoft.com/azure/azure-monitor/app/sampling). By default, adaptive sampling generally only occurs at higher traffic volumes.

### I used to see data but don't anymore

* Check that a deployment has not modified or removed Application Insights configuration or dependecies.
* If you have configured your application to send data through Status Monitor and web published, ensure you don't select the "delete existing files" option during publish.

### I see data in my pre-production/development envirnonment but not production

* Check that you have configured your firewall to allow traffic through the ports required for Application Insights to send data.
* If your instrumentation key is set programmatically or through a configuration file, validate that these values are correct.

If none of these steps resolve your issue, there are more detailed checklists to follow below depending on which SDK or method of application instrumentation you are using.

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)\

* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)\

* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)\

* [Review the complete list of supported SDKs + platforms](https://docs.microsoft.com/azure/application-insights/app-insights-platforms)\