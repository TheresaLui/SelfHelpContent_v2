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

In order to **filter** telemetry you will need to create an [ITelemetryProcessor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#filtering-itelemetryprocessor) and add it to your application code or - for Java applications that are instrumented with Application Insights Java 3.0 agent - use [TelemetryProcessors](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-telemetry-processors). Below is a list of language-specific implementations:

* [.NET/Core](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#example-filters)
* [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-telemetry-processors)
* [Node.JS](https://github.com/Microsoft/ApplicationInsights-JS#build-a-new-extension-for-the-sdk)

### **Adding additional properties**

In order to add **additional properties** you will need to create an [ITelemetryInitializer](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer) and add it to your application code.<br>

Refer to the links below to see the examples for:<br>

* [.NET and .NET Core](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#create-a-telemetry-processor-c)
* [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-telemetry-processors)
* [Node](https://github.com/Microsoft/ApplicationInsights-JS#telemetry-initializers)
* [JavaScript](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#javascript-web-applications)
* [Python](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#opencensus-python-telemetry-processors)


## **Recommended Documents**

* [ITelemetryInitializer Documentation](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer)<br>
* [Node.JS ITelemetryInitializer](https://github.com/Microsoft/ApplicationInsights-JS#telemetry-initializers)<br>
* [.NET/Core ITelemetryProcessor](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#example-filters)<br>
* [Java TelemetryProcessors](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-telemetry-processors)<br>
* [Node.JS ITelemetryPlugin](https://github.com/Microsoft/ApplicationInsights-JS#build-a-new-extension-for-the-sdk)<br>
