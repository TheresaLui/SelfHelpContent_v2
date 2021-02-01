<properties 
    pageTitle="Browser Exceptions or Operations data is incorrect or missing on Failures screen"
    description="I am seeing incorrect data or exceptions or operations data is missing on failures screen"
    infoBubbleText="Here are some things to help with your browser exception and operation data issues"
    service="microsoft.insights"
    resource="components"
    authors="telreach"
    ms.author="marwolff, lxiao"
    selfHelpType="generic"
    articleId="appinsights-browser-exceptions-operations-data-missing"
    productPesIds="15693"
    supportTopicIds="32729580, 32729581"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Browser Exceptions or Operations data is incorrect or missing on Failures screen

### **Where's my data**
We understand it can be frustrating when some or all your data is missing. The following steps have frequently resolved missing data issues. Let us know if it they don’t resolve your issue. 

## **Recommended Steps**

If you configured your application to send data to Application Insights, but aren't seeing the data you expect, try the following steps: 

1. **If you see no data**, validate that your instrumentation key is set correctly through your code or in your configuration file.
2. **If you are missing browser or web page data**, validate that you have added  [Application Insights for JavaScript](https://docs.microsoft.com/azure/azure-monitor/app/javascript) to your application.
3. **If data is coming through**, but occasionally (or often) doesn't match what you expect:
    
    * [Double-check your sampling settings](https://docs.microsoft.com/azure/azure-monitor/app/sampling). For .NET applications, adaptive sampling is on by default, but generally only occurs at higher traffic volumes. 
    * [Browser Exceptions data] Application Insights only tracks uncaught errors. If you have a global error handler, make sure you call `trackException` in it. 

4. **If you have a Single Page Application**, ensure that you have [configured your JavaScript SDK instance to work with Single Page Applications](https://docs.microsoft.com/azure/azure-monitor/app/javascript#single-page-applications). Otherwise, only the first route of your front-end will be tracked. 
5. **If you used to see data but don't anymore**, validate that a deployment has not modified or removed Application Insights configuration or dependencies. If you configured your application to send data through Status Monitor and web published, ensure you do not select the **delete existing files** option during publish. 
6. **If you see data for a pre-production/development environment but not for your production environment**, ensure that you have [configured your firewall to allow traffic through the ports required](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses) for Application Insights to send data. In addition, if your instrumentation key is set programmatically or through a configuration file, validate that these values are correct. 

If none of these simple steps resolve your issue, there are more detailed checklists to follow below depending on which SDK or method of application instrumentation you are using. 

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [using the 2.x SDK without the 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.microsoft.com/azure/azure-monitor/app/monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Monitoring your client-side JavaScript Application](https://docs.microsoft.com/azure/azure-monitor/app/javascript)
* [Review the complete list of supported SDKs + platforms ](https://docs.microsoft.com/azure/azure-monitor/app/platforms)
