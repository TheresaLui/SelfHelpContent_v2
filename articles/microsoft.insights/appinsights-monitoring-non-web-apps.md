<properties
    pageTitle="I need to monitor non-web apps"
    description="How to monitor non-HTTP or background applications in Azure environment"
    service="microsoft.insights"
    resource="components"
    authors="MS-jgol"
    ms.author="Julia Goloshubina"
    articleId="appinsights-monitoring-non-web-apps"
    displayOrder="99"
    selfHelpType="generic"
    cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    productPesIds="15693"
    supportTopicIds="32729599"
    ownershipId="AzureMonitoring_ApplicationInsights"
 />

# <-- appinsights-monitoring-non-web-apps --> \
**Monitoring Non-Web (Non-HTTP/Background) Applications**


## Common issues 
The types of applications that do not use HTTP requests, such as messaging, background, and console applications, cannot utilize Application Insights SDKs or agent designed for web apps. 

## **Recommended Steps**
1. Install the [`Microsoft.ApplicationInsights.WorkerService` SDK](https://www.nuget.org/packages/Microsoft.ApplicationInsights.WorkerService)
1. Follow the guidance for these currently supported scenarios:
    * [.NET Core 3.0 Worker Service applications](https://docs.microsoft.com/azure/azure-monitor/app/worker-service#net-core-30-worker-service-application)
    * [.Net Core Background tasks with hosted services in .Net Core 2.1/2.2](https://docs.microsoft.com/azure/azure-monitor/app/worker-service#aspnet-core-background-tasks-with-hosted-services)
    * [.NET Core/.NET framework console apps in .NET Core 2.0 or higher, and .NET Framework 4.7.2 or higher](https://docs.microsoft.com/azure/azure-monitor/app/worker-service#net-corenet-framework-console-application)

Please note that monitoring non-HTTP applications is currently not supported in Java, Node.js, Python.
