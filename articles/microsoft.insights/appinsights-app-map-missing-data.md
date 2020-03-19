<properties
    pageTitle="Application Map is missing some of the dependencies"
    description="Distributed tracing does not show data from related Azure Monitor Application Insights Resources"
    service="microsoft.insights"
    resource="components"
    authors="MS-jgol"
    ms.author="jgol"
    selfHelpType="generic"
    articleId="appinsights-app-map-missing-data"
    displayOrder="99"
    cloudEnvironments="public, Fairfax, mooncake"
    productPesIds="15693"
    supportTopicIds="32729568"
    ownershipId="AzureMonitoring_ApplicationInsights"
 />

# <-- appinsights-app-map-missing-data -->
**Dependencies are missing from the application map**


## Common issues 
Application Map shows the dependency relationships between your application components and their dependencies. This is true regardless of whether you have configured the components as different roles in a single AI resource, different AI resources or have a mix between these approaches. 

In the diagram below, X, Y and Z are 3 components with dependency relationships between them. <b>If your Application Map for X does not show Y or Z</b>, follow the steps below to diagnose. 

![Dependencies](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/data-collection/app-map.png)

## **Recommended Steps**

1. Change the time range for the map to a longer duration. If the dependency wasn't called in the default time range (last hour) but was called previously – this may be why it wasn't on the map earlier. 
1. Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs. 

### **If Y or Z are modeled as different roles within the same AI resource**
1. Confirm cloud_RoleName is correctly configured for Y or Z. 
1. If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). If not, you can still track it manually with a [track dependency call](https://docs.microsoft.com/azure/application-insights/app-insights-api-custom-events-metrics#trackdependency). 

### **If Y or Z are components and modeled as different AI resources** 
1. Check to see if the "update map components" is failing to light up. This may happen for very large distributed applications. Reducing the time range you are querying for may help here.
1. If you don't see Y (direct HTTP calls): 
    * Upgrade all components to the latest SDK version 
    * If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions) 
1. If you don't see Z (async across a queue): 
This is not supported currently. If X and Z are in the same resource group, as a workaround you can use the map in the [resource group insights experience](https://docs.microsoft.com/azure/azure-monitor/insights/resource-group-insights#diagnose-issues-in-your-resource-group). 
1. If this is Azure Event Hub or Service Bus: Please ensure you are using the latest Azure client SDK to call the queue. 
1. If this is Azure storage queue: Please instrument your calls as described [here](https://docs.microsoft.com/azure/azure-monitor/app/custom-operations-tracking#azure-storage-queue). 

## **Recommended Documents**

* [Application Map](https://docs.microsoft.com/azure/azure-monitor/app/app-map)  
