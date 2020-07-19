<properties
    pageTitle="I am not getting profiler traces"
    description="I am not getting profiler traces"
    service="microsoft.insights"
    resource="components"
    authors="brahmnes"
    ms.author="brahmnes"
    displayOrder="40"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32602204"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	articleId="05d43415-414c-4ea2-be1c-90cc41e48e22"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am not getting profiler traces

## **Recommended Steps**

1. Verify that the profiler is properly configured by following the steps in the article for your app type:

  * [Configure profiler for Azure Web Apps](https://go.microsoft.com/fwlink/?linkid=867935)
  * [Configure profiler for Azure VMs](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
  * [Configure profiler for Service Fabric](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-servicefabric?toc=/azure/azure-monitor/toc.json)
  * [Configure profiler for Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-cloudservice?toc=/azure/azure-monitor/toc.json)
  
2. Verify the profiler traces can be [viewed](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-overview?toc=/azure/azure-monitor/toc.json#view-profiler-data) from the performance blade.<br>

The profiler doesn't collect traces 100% of the time due to resource and performance considerations. For Azure Web Apps, the profiler can be [configured to run manually](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-settings?toc=/azure/azure-monitor/toc.json#profileondemand), which will collect traces for one fixed period of time.

If there are still issues with profiler after trying the steps above, run through [the troubleshooting steps listed here](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-troubleshooting?toc=/azure/azure-monitor/toc.json).<br>

**Known Issues**

If you have AI SDK 2.8.0 or 2.8.1 built into your application and are not running on Azure App Services, the profiler won't work. There is a bug in the version of the profiler that ships with the Windows Azure Diagnostics Extension (WAD). We are working to deploy a fix for the issue. Until then, you can work around it by downgrading your AI SDK to 2.7.2. This is not an issue on Azure App Services. The profiler for App Services has been updated with a fix.

## **Recommended Documents**

* [Profile live Azure web apps with Application Insights](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-overview?toc=/azure/azure-monitor/toc.json)<br>
* [Enable Application Insights Profiler for Azure VMs, Service Fabric, and Cloud Services](https://docs.microsoft.com/azure/application-insights/app-insights-profiler-vm?toc=/azure/azure-monitor/toc.json)
