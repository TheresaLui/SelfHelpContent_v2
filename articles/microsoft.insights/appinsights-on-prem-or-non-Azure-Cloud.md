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

Note that there are two ways to enable Application insights: [Agent or SDK](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview#how-does-application-insights-work). Skip to the recommendations that apply to you.

## **Application Insights Agent Recommended Steps**

Agent-based monitoring is available to monitor [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-overview) and [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-on-premises) applications running on-premises or non-Azure IaaS.

1. Review language-specific troubleshooting guide [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot) for common problems and solutions (ASP.NET Only)
2. Check if the **Azure user** has access to the subscription you are connecting to
3. Check if the **local user** has access to IIS, the registry, and the application folder (ASP.NET Only)
4. Check if the **local machine** is connected to the internet or has a proxy connection, and that the local user has access to the proxy

## **SDK Recommended Steps**

SDK-based monitoring is available to monitor [ASP.NET Core](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-core), [ASP.NET](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net), [Java](https://docs.microsoft.com/en-us/azure/azure-monitor/app/java-get-started?tabs=maven), [Node.JS](https://docs.microsoft.com/en-us/azure/azure-monitor/app/nodejs#get-started), and [Python](https://docs.microsoft.com/en-us/azure/azure-monitor/app/opencensus-python) applications running on-premises, non-Azure IaaS, or non-Azure PaaS.

1. Use agent-based monitoring if supported for your language
2. Updgrade to the latest version of the SDK
3. Review language-specific getting started guide 
4. Review language-specific troubleshooting guide if available (ASP.NET Core, ASP.NET, Java
5. If you can edit the project in Visual Studio, see if you can [install the SDK via NuGet packages](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net?toc=/azure/azure-monitor/toc.json)

* [Application Insights Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-asp-net-troubleshoot-no-data)

## **Recommended Documents**
* [Java On-Premises Overview](https://docs.microsoft.com/en-us/azure/azure-monitor/app/java-on-premises)
* 
