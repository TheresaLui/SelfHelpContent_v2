<properties 
    pageTitle="My app runs on an on-premises server or non-Azure cloud"
    description="General troubleshooting for Status Monitor and SDK"
    service="microsoft.insights"
    resource="components"
    authors="telreach"
    ms.author="mmcc, ramthi"
    articleId="appinsights-on-prem-or-non-Azure-Cloud"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32729616, 32729615"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Issues enabling data collection on-premeses or in a non-Azure cloud

We understand you are encountering issues while enabling application insights on-premises or in a non-Azure cloud. Most commonly this is related to local user permissions, internet access, or Azure subscription permissions.

Note that there are two ways to enable Application insights: [SDK or Agent](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview#how-does-application-insights-work). Skip to the recommendations that apply to you.

## **On-Premises Agent Recommended Steps**

The Status Monitor is an on-premises Windows application that helps with the configuration of an existing ASP.NET application. The Status Monitor does not configure telemetry for Java, nodeJS, JavaScript or service applications. 

1. Review the [troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot) for common problems and solutions
2. Check if the **Azure user** has access to the subscription you are connecting to
3. Check if the **local user** has access to IIS, the registry, and the application folder
4. Check if the **local machine** is connected to the internet or has a proxy connection, and that the local user has access to the proxy
5. If you can edit the project in Visual Studio, see if you can [install the SDK via NuGet packages](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net?toc=/azure/azure-monitor/toc.json)

**Known Issues**

The Status Monitor will attempt to update the assemblies every time the editor UI is started. If you are unable to connect to the internet, it can appear as if the UI is locked up.

## **SDK Recommended Steps**



## **Recommended Documents**
* [Status Monitor](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-performance-live-website-now)
* [Application Insights Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)
