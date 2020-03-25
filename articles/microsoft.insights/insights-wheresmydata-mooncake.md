<properties 
    pageTitle="Where's my data?"
    description="Where's my data?"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    ms.author="mcosner"
    displayOrder="15"
    selfHelpType="resource"
    productPesIds=""
    supportTopicIds=""
    cloudEnvironments="MoonCake"
 	articleId="insights-wheresmydata-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>
 
# Where's my data?

## **Recommended Steps**

If you've configured your application to send data to Application Insights but aren't seeing the data you expect, try the following steps:

1. If you aren't seeing any data at all, validate that your instrumentation key is set correctly through your code or in your configuration file
2. If data is coming through, but occasionally (or often) the data doesn't match what you expect, [double-check your sampling settings](https://docs.azure.cn/azure-monitor/app/sampling). By default, adaptive sampling generally only occurs at higher traffic volumes.
3. If you used to see data but don't anymore, validate that a deployment has not modified or removed Application Insights configuration or dependencies. If you have configured your application to send data through Status Monitor and web published, ensure you do not select the "delete existing files" option during publish.
4. If you see data for a pre-production/development environment but not your production environment, ensure that you have [configured your firewall to allow traffic through the ports required](https://docs.azure.cn/azure-monitor/app/ip-addresses) for Application Insights to send data. In addition, if your instrumentation key is set programmatically or through a configuration file, validate that these values are correct.

If none of these simple steps resolve your issue, there are more detailed checklists to follow below depending on which SDK or method of application instrumentation you are using.

## **Recommended Documents**

* [Troubleshoot issues seeing data with ASP.Net applications](https://docs.azure.cn/azure-monitor/app/asp-net-troubleshoot-no-data)
* [Troubleshoot issues seeing data with Java applications](https://docs.azure.cn/azure-monitor/app/java-troubleshoot)
* [Troubleshoot issues with Application Insights Status Monitor](https://docs.azure.cn/azure-monitor/app/monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights)
* [Review the complete list of supported SDKs + platforms](https://docs.azure.cn/azure-monitor/app/platforms)
