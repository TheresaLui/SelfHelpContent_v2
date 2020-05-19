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
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Dependencies data is incorrect or missing on Application Map

### **Where's my data?**
We understand it can be frustrating when some or all your data is missing. The steps below have frequently resolved missing data issues; please try them out and let us know if it they don’t resolve your issue. 

## **Recommended Steps**

If you've configured your application to send data to Application Insights but aren't seeing the data you expect, try the following steps: 

1. **If you aren't seeing any data at all**, validate that your instrumentation key is set correctly through your code or in your configuration file 
2. **If you are missing Browser or Web page data**, validate that you have added  [Application Insights for JavaScript](https://docs.microsoft.com/azure/azure-monitor/app/javascript) to your application. 
3. **If data is coming through**, but occasionally (or often) the data doesn't match what you expect, Application Insights only tracks XHR requests made from the page, to track fetch API request please configure it on using disableFetchTracking=false.

If none of these simple steps resolve your issue, there are more detailed checklists to follow below depending on which SDK or method of application instrumentation you are using. 

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Java applications](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/azure-monitor/app/monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Monitoring your client-side JavaScript Application](https://docs.microsoft.com/azure/azure-monitor/app/javascript)
* [Review the complete list of supported SDKs + platforms ](https://docs.microsoft.com/azure/azure-monitor/app/platforms)