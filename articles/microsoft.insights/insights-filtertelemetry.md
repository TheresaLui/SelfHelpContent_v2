<properties 
    pageTitle="How do I filter telemetry or add additional properties to my telemetry?"
    description="Getting started doc on how to filter telemetry"
    infoBubbleText="Here is a set of links and concepts to help with this topic."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_filtertelemetry"
    diagnosticScenario="ApplicationInsightsFilterTelemetry"
    displayOrder="1123"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32632989,32729609"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# How do I filter telemetry or add additional properties to my telemetry?

### **Filtering telemetry**

In order to **filter** telemetry you will need to create an [ITelemetryProcessor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#filtering-itelemetryprocessor) ad add it to your application code. Below is a list of specific SDK implementations:

* [.NET/Core](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#example-filters)
* [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-filter-telemetry)
* [Node.JS](https://github.com/Microsoft/ApplicationInsights-JS#build-a-new-extension-for-the-sdk)

### **Adding additional properties**

In order to add **additional properties** you will need to create an [ITelemetryInitializer](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer) and add it to your application code.<br>

[This link](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer) has examples for:<br>

* .NET
* .NET Core
* Java
* JavaScript

[See here](https://github.com/Microsoft/ApplicationInsights-JS#telemetry-initializers) for Node.JS.


## **Recommended Documents**

* [ITelemetryInitializer Documentation](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer)<br>
* [Node.JS ITelemetryInitializer](https://github.com/Microsoft/ApplicationInsights-JS#telemetry-initializers)<br>
* [.NET/Core ITelemetryProcessor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#example-filters)<br>
* [Java ITelemetryProcessor](https://docs.microsoft.com/azure/azure-monitor/app/java-filter-telemetry)<br>
* [Node.JS ITelemetryPlugin](https://github.com/Microsoft/ApplicationInsights-JS#build-a-new-extension-for-the-sdk)<br>
