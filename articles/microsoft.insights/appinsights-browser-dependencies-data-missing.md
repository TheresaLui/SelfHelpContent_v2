<properties 
    pageTitle="Dependencies data is incorrect or missing"
    description="I am seeing incorrect data or dependencies data is missing"
    infoBubbleText="Here are some things to help with your browser dependencies data issues"
    service="microsoft.insights"
    resource="components"
    authors="telreach"
    ms.author="hectorh"
    selfHelpType="generic"
    articleId="appinsights-browser-dependencies-data-missing"
    productPesIds="15693"
    supportTopicIds="32729579"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Dependencies data is incorrect or missing on Application Map

### **Where's my data?**
We understand it can be frustrating when some or all of your data is missing. The following steps have frequently resolved missing data issues. Please try them and let us know if they don’t resolve your issue. 

## **Recommended Steps**

If you configured your application to send data to Application Insights, but aren't seeing the data you expect, try these steps: 

1. **If you have no data**, validate that your instrumentation key is set correctly through your code or in your configuration file. 
2. **If you are missing browser or web page data**, validate that you have added  [Application Insights for JavaScript](https://docs.microsoft.com/azure/azure-monitor/app/javascript) to your application. 
3. **If data is coming through**, but occasionally (or often) doesn't match what you expect, Application Insights only tracks XHR requests made from the page. To track fetch API requests, configure it on using `disableFetchTracking=false`.

If none of these simple steps resolve your issue, review the detailed checklists in the **Recommended Documents** that apply to the SDK or method of application instrumentation you use. 

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [using the 2.x SDK without the 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/azure-monitor/app/monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Monitoring your client-side JavaScript Application](https://docs.microsoft.com/azure/azure-monitor/app/javascript)
* [Review the complete list of supported SDKs + platforms ](https://docs.microsoft.com/azure/azure-monitor/app/platforms)
