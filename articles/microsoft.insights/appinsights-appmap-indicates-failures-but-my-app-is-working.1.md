<properties
    pageTitle="Application Map indicates failures, but my app is working"
    description="Application Map indicates failures, but my app is working"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="appinsights-appmap-indicates-failures-but-my-app-is-working"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729573"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- appmap-indicates-failures-but-my-app-is-working -->

Application map shows failures and a component as red based on a failure threshold of 0.1%. These represent the failures that might be causing your apps to fail. In case you are in a situation, where you feel your app is working fine but the map seems full of failures, then follow one of the recommended steps below.

## **Recommended solutions**

### 1. **Filter out 4xx errors on Map** 

* Application Map has a toggle for filtering out errors 4xx class error codes. Switch the toggle to on to exclude these 400 class errors from your application map.

![appmap image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-map-indicates-failure-but-my-app-works.png)

### 2. **Go to failure blade to investigate failures** 

* To understand what failures are occurring that’s causing your application map to be filled with errors, navigate to failure blade. This will give you insight on what failures you are seeing, and you can decide whether they contribute to your application’s failures or not. Please follow [instruction here](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-exceptions#diagnosing-failures-using-the-azure-portal).  


## **Recommended Documents**

* [Application Map details](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-map?tabs=net)<br>
* [Failure blade](https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-exceptions#diagnosing-failures-using-the-azure-portal)<br>
