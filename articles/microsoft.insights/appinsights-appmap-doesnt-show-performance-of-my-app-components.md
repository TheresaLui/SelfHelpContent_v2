<properties
    pageTitle="Application Map doesn't show performance of my app's components"
    description="Application Map doesn't show performance of my app's components"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="appinsights-appmap-doesnt-show-performance-of-my-app-components"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729571"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- appinsights-appmap-doesnt-show-performance-of-my-app-components -->

Application Map helps you spot performance bottlenecks or failure hotspots across all components of your distributed application. Sometimes because of various reasons Application Map doesn’t work the way its supposed to like not showing performance. Following below steps should help you troubleshoot:


## **Recommended Steps**


* Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs.

* Upgrade all components to the latest SDK version
* If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* Confirm [cloud_RoleName](https://docs.microsoft.com/azure/azure-monitor/app/app-map#Set-cloud-RoleName) is correctly configured.

## **Recommended Documents**

* [Application Map Troubleshooting](https://docs.microsoft.com/azure/azure-monitor/app/app-map#troubleshooting)

