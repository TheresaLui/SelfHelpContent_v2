<properties
    pageTitle="Application Map doesn't show dependencies"
    description="Application Map doesn't show dependencies"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="appinsights-appmap-doesnt-show-dependencies"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729568"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- appinsights-appmap-doesnt-show-dependencies -->

A dependency is an external component that is called by your application. It's typically a service called using HTTP, or a database, or a file system. Sometimes, they fail to show up on a map for various reasons below:

![appmap image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-map-dependencies.png)

## **Recommended Steps**

### 1. **Select a longer time range** 

* Increase the time duration on the map to check if the component appears as it may not have been called in the last hour but might appear for a longer duration selected. 

### 2. **Check Auto collected dependency** 

* If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). This page gives list of dependency calls that are automatically detected as dependencies.

* There are some dependencies that are not automatically collected by SDK, you can track them manually using the [TrackDependency API](https://docs.microsoft.com/azure/azure-monitor/app/api-custom-events-metrics#trackdependency) 

### 3. **Dependencies are application components thar are in a separate resource**

* Check to see if the **update map components** button is failing to light up. This may happen for very large distributed applications. Reducing the time range you are querying for may help here.
* Ensure that that you have [permissions](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control#to-provide-access-to-another-user) to the App Insights resource with other components of the application.
* If you don’t see Z (direct HTTP calls):
    * Upgrade all components to the latest SDK version
    * If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* If you don’t see Y (async across a queue): 
    * Click on *Try* button on the purple banner on the top to try preview of App Map that provides this cross-component tracing across supported queues only. Note: This is a preview version only.  

![appmap dependency image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-map-not-showing-data-from-related-resources.png)

### 4. **Check Cloud RoleName configuration**
* If dependencies are application components, modeled as different roles
within the same AI resource: Confirm [cloud_RoleName](https://docs.microsoft.com/azure/azure-monitor/app/app-map#Set-cloud-RoleName) is correctly configured.


## **Recommended Documents**

* [Dependency Auto-collection](https://docs.microsoft.com/azure/azure-monitor/app/auto-collect-dependencies)
* [Manually Track dependency](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-dependencies#manually-tracking-dependencies)
* [Application Map Troubleshooting](https://docs.microsoft.com/azure/azure-monitor/app/app-map#troubleshooting)

