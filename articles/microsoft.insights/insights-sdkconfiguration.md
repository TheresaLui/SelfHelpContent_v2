<properties 
    pageTitle="How do I configure my SDK?"
    description="Will give locations and instructions on how to configure the SDK"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_sdkconfiguration"
    displayOrder="102"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602223"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# How do I configure my SDK?

## **Recommended Steps**

1. Ensure you have the latest versions of Application Insights installed
2. Follow the getting started document for your version of the SDK
3. Start over with a fresh install and compare the differences
4. Review your config file with a specific topic below

**If you are recieving SDK errors**

For all supported SDKs you should not see any errors relating to telemetry collection. If you are seeing errors that are specific to **dc.services.visualstudio.com**, please use the steps below. If you are seeing other errors coming from your application, please go back and open a case for the SDK.

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)
2. If the errors are inside of your telemetry, please go back and open a case for the correct SDK
3. If you are receiving an error message from the service, it is likely that we are experiencing issues and it is recommended to open a case for tracking

## **Recommended Documents**

### **.NET Configuration Topics**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/asp-net)
* [Adaptive Sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling#adaptive-sampling-at-your-web-server)
* [Telemetry Processors](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling)
* [Dependency Tracking](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-dependencies#set-up-dependency-monitoring)
* [Configuration Reference](https://docs.microsoft.com/azure/azure-monitor/app/configuration-with-applicationinsights-config)

### **Java Configuration Topics**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started)
* [Sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling#configuring-fixed-rate-sampling-in-java)
* [Telemetry Processors](https://docs.microsoft.com/azure/azure-monitor/app/java-filter-telemetry)
* [Dependency Tracking](https://docs.microsoft.com/azure/azure-monitor/app/java-agent)
* [Configuration Reference](https://github.com/Microsoft/ApplicationInsights-Java/wiki/ApplicationInsights.XML)

### **JavaScript Configuration Topics**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/javascript)
* [Sampling](https://docs.microsoft.com/azure/azure-monitor/app/sampling#sampling-for-web-pages-with-javascript)
* [Telemetry Initializers](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#addtelemetryinitializer)
* [Configuration Reference](https://github.com/Microsoft/ApplicationInsights-JS/blob/master/API-reference.md#config)

### **Node.JS Configuration Topics**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/nodejs)
* [Sampling](https://github.com/Microsoft/ApplicationInsights-node.js/#sampling)
* [Telemetry Processors](https://github.com/Microsoft/ApplicationInsights-node.js/#preprocess-data-with-telemetry-processors)
* [Configuration Reference](https://github.com/Microsoft/ApplicationInsights-node.js/#advanced-configuration-options)
