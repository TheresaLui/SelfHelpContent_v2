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
 
# Issues enabling data collection on-premises or in a non-Azure cloud

We understand you are encountering issues while enabling application insights on-premises or in a non-Azure cloud. Most commonly this is related to local user permissions, internet access, or Azure subscription permissions.

Note that there are two ways to enable Azure Monitor's Application insights: [Agent or SDK](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview#how-does-application-insights-work). Skip to the section that applies to you.

## **Application Insights Agent Recommended Steps**

Agent-based monitoring is available to monitor [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-overview) and [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-on-premises) applications running on-premises or non-Azure IaaS.

1. Review language-specific agent troubleshooting guide if available ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot), Java (Not Available))
2. Check if the **Azure user** has access to the subscription you are connecting to
3. Check if the **local user** has access to IIS, the registry, and the application folder (ASP.NET Only)
4. Check if the **local machine** is connected to the internet or has a proxy connection, and that the local user has access to the proxy

## **Application Insights SDK Recommended Steps**

SDK-based monitoring is available to monitor [ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started?tabs=maven), [Node.JS](https://docs.microsoft.com/azure/azure-monitor/app/nodejs#get-started), and [Python](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) applications running on-premises, non-Azure IaaS, or non-Azure PaaS.

1. Use agent-based monitoring if supported for your language
2. Upgrade to the latest version of the SDK
3. Review language-specific SDK troubleshooting guide if available ([ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot), Node.JS (Not Available), Python (Not Available).

## **Recommended Documents**
* [Application Insights FAQ](https://docs.microsoft.com/azure/azure-monitor/faq#application-insights)
* Agent Getting Started Guides ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-overview), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-on-premises))
* Agent Troubleshooting Guides ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot))
* SDK Getting Started Guides  ([ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started?tabs=maven), [Node.JS](https://docs.microsoft.com/azure/azure-monitor/app/nodejs#get-started), [Python](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python))
* SDK Troubleshooting Guides ([ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot))
