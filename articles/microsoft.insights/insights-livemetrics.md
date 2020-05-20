<properties 
    pageTitle="Why can I not see Live Metrics?"
    description="Troubleshooting steps for Live Metrics stream"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_livemetrics"
    displayOrder="100"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602207"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Why can I not see Live Metrics?

Live Metrics is an addon to the .NET and Java SDK frameworks that allows real time monitoring (in seconds instead of minutes) of your application. This feature works by opening a connection to an endpoint and sending aggregate data at a high rate. If you are unable to see Live Metrics, it is most commonly because module/setting is missing from the config file and firewall.<br>

## **Recommended Steps**

**Firewall**<br>

1. [Review the IP addresses used by insights and analytics](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses)
2. Contact your IT team to open a rule to allow port 443 over TCP

**Missing Config .NET**<br>

1. Verify you're using version 2.4.0-beta2 or greater
2. Edit the ApplicationInsights.config file
3. Locate the [QuickPulseTelemetryModule](https://github.com/Microsoft/ApplicationInsights-Home/blob/045ed7325d115c0f239757690faccb44dbeb453b/Samples/PingMeshWeb/PingMeshWeb/ApplicationInsights.config#L7)config option; if it is not there add it
4. Locate the [QuickPulseTelemetryProcessor](https://github.com/Microsoft/ApplicationInsights-Home/blob/045ed7325d115c0f239757690faccb44dbeb453b/Samples/PingMeshWeb/PingMeshWeb/ApplicationInsights.config#L28) config option; if it is not there add it
5. Restart the application

**Missing Config Java**<br>

1. Verify you're using version 1.0.8 or greater (2.1.0+ recommended)
2. Edit the ApplicationInsights.xml file
3. Locate the [QuickPulse](https://github.com/Microsoft/ApplicationInsights-Java/blob/40809cb6857231e572309a5901e1227305c27c1a/core/src/test/resources/ApplicationInsights2.xml#L132) config option; if it is not there add it
4. Locate the [QuickPulseTelemetryProcessor](https://github.com/Microsoft/ApplicationInsights-Home/blob/045ed7325d115c0f239757690faccb44dbeb453b/Samples/PingMeshWeb/PingMeshWeb/ApplicationInsights.config#L28); if it is not there add it

### **Known Issues**

* Live Metrics is not supported on Node.JS. Please upvote [this uservoice](https://feedback.azure.com/forums/357324-application-insights/suggestions/18622672-live-metrics-support-for-node-js) to show interest.<br>
* Requires Application Insights .NET SDK version 2.4.0-beta2 or greater
* Requires Java Version 1.0.8 or greater<br> 
* The native Java SDK does not have full parity with all Live Metrics features. You should consider using the [local forwarder](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#local-forwarder)<br> 

## **Recommended Documents**

* [Live Metrics](https://docs.microsoft.com/azure/azure-monitor/app/live-stream)
