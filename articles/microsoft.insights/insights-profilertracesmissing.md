<properties
    pageTitle=".NET Profiler traces are missing."
    description="This topic will help you diagnose missing profile traces."
    service="microsoft.insights"
    resource="components"
    authors="cweining"
    ms.author="cweining"
    displayOrder="40"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32729565"
    cloudEnvironments="public, Fairfax, Mooncake"
     articleId="insights-profilertracesmissing"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am not getting profiler traces

If you don't have any profile traces available to view from the App Insights Performance or End to End Transaction page

There are two main reasons why you might not have any profile traces available to view from the Performance or End to End transaction page. First, Profiler must be enabled for your application. Second, there has to be traffic to your application while the profiler is running and it doesn't run all of the time.

## **Recommended Steps**

1. Verify that the profiler is properly configured by following the steps in the article for your app type:

  * [Configure profiler for Azure Web Apps](https://go.microsoft.com/fwlink/?linkid=867935)
  * [Configure profiler for Azure VMs](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
  * [Configure profiler for Service Fabric](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-servicefabric?toc=/azure/azure-monitor/toc.json)
  * [Configure profiler for Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-cloudservice?toc=/azure/azure-monitor/toc.json)
  
2. Verify the profiler traces can be [viewed](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-overview?toc=/azure/azure-monitor/toc.json#view-profiler-data) from the performance blade.<br>

The profiler doesn't collect traces 100% of the time due to resource and performance considerations. The profiler can be [configured to run manually](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-settings?toc=/azure/azure-monitor/toc.json#profileondemand), which will collect traces for one fixed period of time.

If there are still issues with profiler after trying the steps above, run through [the troubleshooting steps listed here](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-troubleshooting?toc=/azure/azure-monitor/toc.json).<br>



## **Recommended Documents**

* [Profile live Azure web apps with Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-overview?toc=/azure/azure-monitor/toc.json)<br>
* [Enable Application Insights Profiler for Azure VMs, Service Fabric, and Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
