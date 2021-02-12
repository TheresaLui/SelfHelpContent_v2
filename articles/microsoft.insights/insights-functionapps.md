<properties 
    pageTitle="How do I setup Application Insights with my Function App?"
    description="Getting started doc on how to enable Application Insights with your Function App"
    infoBubbleText="Here is a set of links and concepts to help with this topic."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_functionapp"
    diagnosticScenario="ApplicationInsightsFunctionApp"
    displayOrder="1124"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32729621"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Enabling Application Insights for app that runs on Azure Functions

## **Recommended Steps**

1. Follow the [enable Application Insights integration](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#enable-application-insights-integration) guide
2. Verify the correct Application Insights instance is listed in the **Monitor** section
3. Validate the **APPINSIGHTS_INSTRUMENTATIONKEY** is correct in your **Application Settings**

### **Common Questions**

**What is auto collected?**<br>
FunctionApps v2 will auto collect HTTP, ServiceBus and SQL dependencies for .NET Applications. [See here](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#dependencies) for information.
For Java applications running on Azure Functions, the distributed tracing can be enabled - [follow the instructions here](https://docs.microsoft.com/azure/azure-monitor/app/monitor-functions).<br>

**Missing or partial data**<br>
Sampling is enabled by default which can make it appear as if some data is not being sent. [Click here](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#configure-sampling) for information.<br>

The [log configuration settings](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-configuration-in-hostjson) in your host.json can cause certain data to disappear from Application Insights. For example, if you set [Host.Results](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#category-hostresults) to **Warning** you will not see your executions as server requests.<br>

**Custom Logs and Telemetry**<br>
To write custom logs see the [write logs in C# functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#write-logs-in-c-functions) or [write logs in JavaScript functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#write-logs-in-javascript-functions) documentation.<br>

To create custom telemetry see the [log custom telemetry in C# functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-custom-telemetry-in-c-functions) or [log custom telemetry in JavaScript functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-custom-telemetry-in-javascript-functions)

## **Recommended Documents**

* [Enable Application Insights integration](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#enable-application-insights-integration)<br>
* [Log configuration settings](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-configuration-in-hostjson)<br>
* [Host.Results](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#category-hostresults)<br>
* [Write logs in C# functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#write-logs-in-c-functions)<br>
* [Write logs in JavaScript functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#write-logs-in-javascript-functions)<br>
* [Log custom telemetry in C# functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-custom-telemetry-in-c-functions)<br>
* [Log custom telemetry in JavaScript functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring#log-custom-telemetry-in-javascript-functions)<br>
* [Enable distributed tracing for Java applications](https://docs.microsoft.com/azure/azure-monitor/app/monitor-functions)
