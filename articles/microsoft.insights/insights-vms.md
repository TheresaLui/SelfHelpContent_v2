<properties 
    pageTitle="How to set up Application Monitoring for apps running on Azure VMs and VMSS?"
    description="Getting started doc on how to enable Application Insights with your Azure VM or VMSS apps"
    infoBubbleText="Here is a set of links and concepts to help with this topic."
    service="microsoft.insights"
    resource="components"
    authors="MS-jgol"
    ms.author="jgol"
    articleId="insights_vms"
    diagnosticScenario="ApplicationInsightsVMsVMSS"
    displayOrder="1124"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32681521"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Enabling Application Insights for apps that run on Azure VMs/VMSS

## **Recommended Steps**

### Enable Application Insights without instrumenting the code - .Net and Java
Note that both of the codeless solutions are currently in public preview, and fully supported.
For .Net and Java Application Insights can be enabled without any code change with just a few easy steps:
1. For .Net, follow the [deploy the Azure Monitor Application Insights agent](https://docs.microsoft.com/azure/azure-monitor/app/azure-vm-vmss-apps) guide. 
1. For Java apps, follow the [codeless application monitoring with Azure Monitor Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/java-in-process-agent) documentation
1. For .Net Core, Node.js, and Python only SDK instrumentation is available

### Enable Application Insights with the SDKs - .Net Core, Node.js, and Python
Follow the guidelines below:
1. [To instrument a .Net Core application](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core)
1. [To enable Application Insights for a Node.js app](https://docs.microsoft.com/azure/azure-monitor/app/nodejs)
1. [To monitor Python applications](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)


## **Recommended Documents**

* [Application Insights FAQ](https://docs.microsoft.com/azure/azure-monitor/faq#application-insights)
