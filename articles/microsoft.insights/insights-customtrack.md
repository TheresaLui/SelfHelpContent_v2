<properties 
    pageTitle="Issue tracking additional telemetry (dependencies, exceptions, etc.)"
    description="General troubleshooting guide for custom instrumentation"
    service="microsoft.insights"
    resource="components"
    authors="osvaldorosado"
    ms.author="osrosado"
    articleId="insights-customtrack"
    displayOrder="97"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32729612"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Issue tracking additional telemetry (dependencies, exceptions, etc.)

## **Recommended Steps**

Application Insights SDKs provide several methods to augment automatically collected telemetry with additional, manually tracked telemetry. These methods vary by SDK, but typically follow common patterns between different platforms.

Follow the guide in [Application Insights API for custom events and metrics](https://docs.microsoft.com/azure/azure-monitor/app/api-custom-events-metrics) to walk through methods for calling manual telemetry tracking on your chosen SDK.

Note that Application Insights SDKs typically do not throw exceptions on errors. When applicable, errors may be printed to your debug console.

### **I need to track additional telemetry in Azure Functions**

Review these guides to track additional telemetry in Azure Functions, depending on the language used:

* [C#](https://docs.microsoft.com/azure/azure-functions/functions-monitoring?tabs=cmd#log-custom-telemetry-in-c-functions)
* [JavaScript](https://docs.microsoft.com/azure/azure-functions/functions-monitoring?tabs=cmd#log-custom-telemetry-in-javascript-functions)
* Track [additional dependencies with Java](https://docs.microsoft.com/azure/azure-monitor/app/monitor-functions) on Azure Functions

### **How do I see debugging information while adding additional telemetry?**

During debugging, use **Developer Mode** to expedite telemetry sending and emit additional debugging information. [Learn more about enabling Developer Mode](https://docs.microsoft.com/azure/azure-monitor/app/api-custom-events-metrics#debug).

### **I'm seeing errors when sending telemetry**
If you are seeing errors that are specific to **dc.services.visualstudio.com**, use the following steps.

1. Verify the version of the SDK you are using is up to date and officially supported (.Net, .NetCore, Java, Node.js, Python, JavaScript)
2. If the errors are inside of your telemetry, open a case for the correct language
3. If you are receiving an error message from the service, it is likely that we are experiencing issues. We recommend that you open a case for tracking.

## **Recommended Documents**

* [Application Insights API for custom events and metrics](https://docs.microsoft.com/azure/azure-monitor/app/api-custom-events-metrics)
