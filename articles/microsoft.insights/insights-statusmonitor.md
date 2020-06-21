<properties 
    pageTitle="I am having problems with the Status Monitor"
    description="General troubleshooting guide for the Status Monitor"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_statusmonitor"
    displayOrder="91"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32629553"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# I am having problems with the Status Monitor

The Status Monitor is an on-premises Windows application that helps with the configuration of an existing ASP.NET application. Most of the issues are related to either local user permissions, internet access, or Azure subscription permissions. The Status Monitor does not configure telemetry for Java, nodeJS, JavaScript or service applications. 

## **Recommended Steps**

1. Review the [troubleshooting guide](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now#troubleshooting-runtime-configuration-of-application-insights) for common problems and solutions
2. Check if the **Azure user** has access to the subscription you are connecting to
3. Check if the **local user** has access to IIS, the registry, and the application folder
4. Check if the **local machine** is connected to the internet or has a proxy connection, and that the local user has access to the proxy
5. If you can edit the project in Visual Studio, see if you can [install the SDK via NuGet packages](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net?toc=/azure/azure-monitor/toc.json)

**Known Issues**

The Status Monitor will attempt to update the assemblies every time the editor UI is started. If you are unable to connect to the internet, it can appear as if the UI is locked up.


## **Recommended Documents**
* [Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now)
* [Application Insights Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)
