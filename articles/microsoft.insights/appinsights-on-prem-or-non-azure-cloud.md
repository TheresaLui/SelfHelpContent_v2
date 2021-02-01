<properties 
    pageTitle="My app runs on an on-premises server or non-Azure cloud"
    description="General troubleshooting for Status Monitor and SDK"
    service="microsoft.insights"
    resource="components"
    authors="telreach"
    ms.author="mmcc, ramthi"
    articleId="appinsights-on-prem-or-non-Azure-Cloud"
    selfHelpType="generic"
    cloudEnvironments="public, fairfax, mooncake, blackforest, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32729616, 32729615"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Issues enabling data collection on-premises or in a non-Azure cloud

We understand you are encountering issues while enabling application insights on-premises or in a non-Azure cloud. Most commonly this is related to local user permissions, internet access, or Azure subscription permissions.

You can enable Azure Monitor's Application insights one of two ways: [Agent or SDK](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview#how-does-application-insights-work). We recommend the agent-based approach, if it's supported for your scenario.

## **Recommended Steps**

1. Confirm that your language is supported for your enablement method:

    - Agent-based: [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-overview) and [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-on-premises)
    - SDK-based:  [ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started?tabs=maven), [Node.JS](https://docs.microsoft.com/azure/azure-monitor/app/nodejs#get-started), and [Python](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)

2. Review the language-specific troubleshooting guide for your enablement method, if available:

    - Agent-based: [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot)
    - SDK-based: [ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot), Node.JS (Not Available), Python (Not Available)

3. Upgrade to the latest version of the SDK or Agent
4. Check if the **Azure user** has access to the subscription where the Application Insights resource resides
5. Check if the **local user** has access to IIS, the registry, and the application folder (ASP.NET Only)
6. Check if the **local machine** is connected to the internet or has a proxy connection, and that the local user has access to the proxy
7. Verify that your firewall has the required [outgoing ports](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses) open to reach the Application Insights endpoint
 
## **Recommended Documents**

* [Application Insights FAQ](https://docs.microsoft.com/azure/azure-monitor/faq#application-insights)
* Agent Getting Started Guides ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-overview), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-on-premises))
* Agent Troubleshooting Guides ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/status-monitor-v2-troubleshoot))
* SDK Getting Started Guides  ([ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [Java](https://docs.microsoft.com/azure/azure-monitor/app/java-get-started?tabs=maven), [Node.JS](https://docs.microsoft.com/azure/azure-monitor/app/nodejs#get-started), [Python](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python))
* SDK Troubleshooting Guides ([ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data), [Application Insights Java 3.0](https://docs.microsoft.com/azure/azure-monitor/app/java-standalone-troubleshoot) or [Java 2.x SDK without 3.0 agent](https://docs.microsoft.com/azure/azure-monitor/app/java-troubleshoot))
* [IP addresses used by Application Insights and Log Analytics](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses)

