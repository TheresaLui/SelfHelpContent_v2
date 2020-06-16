<properties
    pageTitle="Application map doesn’t show data from related AppInsights resources"
    description="Application map doesn’t show data from related AppInsights resources"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="Application map doesn’t show data from related AppInsights resources"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729567"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- Application map doesn’t show data from related AppInsights resources -->

Application Map shows the dependency relationships between your application components and their dependencies. This is true regardless of whether you have configured the components as different roles in a single AI resource, different AI resources or have a mix between these approaches.

In the diagram below, X, Y and Z are 3 components with dependency relationships between them. If your Application Map for X does not show Y or Z, follow the steps below to diagnose.

![appmap image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/missing-data-point-line-chart.png)

## **Recommended solutions**

### 1. **If Y or Z are application components in a different Application Insights resource:**

* Check to see if the “update map components” button is failing to light up. This may happen for very large distributed applications. Reducing the time range you are querying for may help here.
* •	Ensure that that you have [permissions](https://docs.microsoft.com/en-us/azure/azure-monitor/app/resources-roles-access-control#to-provide-access-to-another-user) to the App Insights resource with other components of the application.
* •	If you don’t see Y (direct HTTP calls):
    * Upgrade all components to the latest SDK version
    * If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* If you don’t see Z (async across a queue): This is not supported currently. If X and Z are in the same resource group, as a workaround you can use the map in the [resource group insights experience](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/resource-group-insights#diagnose-issues-in-your-resource-group).


### 2. **Check Auto collected dependency ** 

* If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). This page gives list of dependency calls that are automatically detected as dependencies without requiring any additional modification to your application's code.

* There are some dependencies that are not automatically collected by SDK, you can track them manually using the [TrackDependency API](https://docs.microsoft.com/en-us/azure/azure-monitor/app/api-custom-events-metrics#trackdependency) that is used by the standard auto collection modules. Below are examples of dependencies which are not automatically collected:
    * Azure Cosmos DB is tracked automatically only if HTTP/HTTPS is used. TCP mode won't be captured by Application Insights.
    * Redis

### 3. **Select a longer time range** 

* Increase the time duration on the map to check if the component appears as it may not have been called in the last hour but might appear for a longer duration selected. 

### 4. **Using the supported SDK**  

* Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs.

### 5. **Check Cloud RoleName configuration**

* If dependencies are application components, modeled as different roles
within the same AI resource: Confirm [cloud_RoleName](https://docs.microsoft.com/azure/azure-monitor/app/app-map#Set-cloud-RoleName) is correctly configured.


## **Recommended Documents**

* [Application Map Troubleshooting](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-map#troubleshooting)