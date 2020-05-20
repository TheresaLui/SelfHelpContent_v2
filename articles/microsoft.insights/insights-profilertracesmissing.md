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
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
     articleId="insights-profilertracesmissing"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am not getting profiler traces

There are two main reasons things to check when you don't have profile traces available from the Performance or End to End transaction page. First, profiler must be enabled for your application. Second, there has to be traffic to your application while the profiler is running. If that doesn't solve your problem, checkout our troubleshooting guide.

## **Recommended Steps**

1. Verify that the profiler is properly configured by following the steps in the article for your app type:
    * [Configure profiler for Azure Web Apps](https://go.microsoft.com/fwlink/?linkid=867935)
    * [Configure profiler for Azure VMs](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
    * [Configure profiler for Service Fabric](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-servicefabric?toc=/azure/azure-monitor/toc.json)
    * [Configure profiler for Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-cloudservice?toc=/azure/azure-monitor/toc.json)

1. The profiler doesn't collect traces 100% of the time due to resource and performance considerations. The profiler can be [run on demand](https://docs.microsoft.com/azure/azure-monitor/app/profiler-settings?toc=%2Fazure%2Fazure-monitor%2Ftoc.json#profile-now), which will collect traces for one fixed period of time. When running on demand, be sure you are generating traffic or requests to your application.

1. [Use our troubleshooting guide](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-troubleshooting?toc=/azure/azure-monitor/toc.json) if there are still issues with the profiler after trying the steps above.

## **Recommended Documents**

* [Profile live Azure web apps with Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-overview?toc=/azure/azure-monitor/toc.json)<br>
* [Enable Application Insights Profiler for Azure VMs, Service Fabric, and Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
