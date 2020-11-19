<properties
    pageTitle="Can't enable Application Insights for applications running on Azure App Service"
    description="Enabling troubleshooting of Application Insights monitoring apps hosted on Azure App Services"
    service="microsoft.insights"
    resource="components"
    authors="MS-jgol"
    ms.author="jgol"
    articleId="insights_appservice"
    displayOrder="99"
    selfHelpType="generic"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    productPesIds="15693" 
    supportTopicIds="32729619"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

<!-- appinsights-enable-platform-appservice -->
# **Cannot enable Application Insights for my app running on Azure App Service**

## Common issues

1. The Application Insights option is grayed out and not clickable:

![Application Insights Menu Item](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/data-collection/appinsights-disabled.png)

2. The Application Insights option is clickable, but it is not possible to advance beyond the options screen

## **Recommended Steps**

### **If the Application Insights option is grayed out**

1. The specified language/tech stack may not be supported. Here is what you need to know: 

    * Currently you can enable codeless integration with Application Insights for .Net, .NetCore, Java and Node.js (public preview on Linux and private preview on Windows)
    * For Python you would need to add SDK to your code

### **If the Application Insights option is clickable, but you can't advance beyond the first screen**

1. You are using a free subscription AND happen to have Application Insights enabled for other resources: 

![Application Insights Plan](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/data-collection/appinsights-plan.png) 

Try this:

* [**Easiest**] Change the subscription level
* [**Cheapest**] Disable Application Insights for the other resource first

2. The OS and runtime combination you selected is not supported

## **Recommended Documents**

* [Monitoring an App Service resource](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps)

<!-- To do: add a link to supported languages/frameworks/features when the doc is fixed!! -->
