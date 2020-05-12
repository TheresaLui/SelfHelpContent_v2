<properties 
    pageTitle="How do I investigate errors with the Performance and Failures blade?"
    description="Instructions on how to troubleshoot no data, or errors using the performance and failures blade"
    infoBubbleText="Here is a set of links and concepts to help with this topic."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_performanceandfailures"
    diagnosticScenario="PerformanceAndFailures"
    displayOrder=""
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32632997"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# How do I investigate errors with the Performance and Failures blade?

## **Recommended Steps**

### **Issues with data visualization Performance and/or Failures UI**

Data for these blades are generated from the data that is present in Log Analytics. If you're not seeing the data you expect follow this troubleshooting list to validate that the data is being sent to your instance.

1. Ensure you're using one of the latest Application Insights SDKs:

    - [.NET](https://github.com/microsoft/ApplicationInsights-dotnet/releases/latest)
    - [Java](https://github.com/microsoft/ApplicationInsights-Java/releases/latest)
    - [JavaScript](https://github.com/microsoft/ApplicationInsights-JS/releases/latest)
    - [Node.JS](https://github.com/microsoft/ApplicationInsights-node.js/releases/latest)

2. Try to refresh the data using the **Refresh** button after a minute:

    - Queries are cached for performance

2. Set a larger time range to query a more inclusive set of data:

    - The issue may have occurred just outside of the time boundary
    - Queries are cached based on time range and type, this will pull fresh data in most cases

3. Check the time zone in the time range selector:

    - Set to UTC or Local depending on when the issue occurred

4. Click the **View in Logs** button:

    - This will verify that data is making it to your Application Instance
    - If data is missing after a recent change, follow the [troubleshoot missing data](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data) guide
    - If the data is missing for a short period of time, please check the [outage blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for notifications

5. Check for issues connecting to any Azure endpoints:

    - If you have a proxy or firewall open connections to the [Application Insights API](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#application-insights-api) and the [Application Insights Azure portal Extension](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#application-insights-azure-portal-extension)

### **Issues with your application's performance or errors**

We have a number of documents with examples that you can follow to help investigate issues with your application using Application Insights. Take a look at these resources below to get started investigating issues.

* [Transaction Diagnostics](https://docs.microsoft.com/azure/azure-monitor/app/transaction-diagnostics)
* [Diagnose dependencies](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-dependencies)<br>
* [Diagnose web apps with Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-exceptions)<br>
* [Diagnose run-time exceptions](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-runtime-exceptions)<br>
* [Diagnose performance issues](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-performance)<br>
* [Monitor and alert on application health](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-alert)<br>
* [Understand how customers are using your application](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-users)<br>
* [Debug snapshots on exceptions](https://docs.microsoft.com/azure/azure-monitor/app/snapshot-debugger)<br>
* [Explore trace logs](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-trace-logs)<br>
