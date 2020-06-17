<properties
    pageTitle="Application Map doesn't show some of my app components"
    description="Application Map doesn't show some of my app components"
    service="microsoft.insights"
    resource="components"
    authors="rishabjolly"
    ms.author="rijolly"
    displayOrder="2"
    articleId="aappinsights-appmap-doesnt-show-some-of-my-app-components"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32729572"
    resourceTags=""
    productPesIds="15693"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# <-- appinsights-appmap-doesnt-show-some-of-my-app-components -->

Application map displays your app components and dependencies. These app components are independently deployable parts of your distributed/microservices application and can be within the same AI resource or a different AI resource. Sometimes, they fail to show up on a map for various reasons below:

![appmap image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-map-doesnt-show-some-of-my-app-components.png)

## **Recommended solutions**

### 1. **If the components are in same App Insights resources with direct calls being made between the components:** 

* Increase the time duration on the map to check if the component appears as it may not have been called in the last hour but might appear for a longer duration selected. 
* If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/en-us/azure/azure-functions/functions-versions).
* Confirm [cloud role name](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-map#set-cloud-role-name) is correctly configured


### 2. **If the components are in different App Insights resources with direct calls being made between the components:** 

* Sometimes the components are in different Application Insights resources. In that case clicking button **Update Map Components** in the top-left corner of the map will update with the number of components in your application as they are discovered. 
* Ensure that that you have [permissions](https://docs.microsoft.com/en-us/azure/azure-monitor/app/resources-roles-access-control#to-provide-access-to-another-user) to the App Insights resource with other components of the application. 


### 3. **Using the supported SDK**  

* Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs.

### 4. **Check Auto collected dependency**

* If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). If not, you can still track it manually with a [track dependency call](https://docs.microsoft.com/azure/application-insights/app-insights-api-custom-events-metrics#trackdependency).


## **Recommended Documents**

* [Troubleshooting Application Map](https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-map#troubleshooting)
* [Telemetry correlation](https://docs.microsoft.com/en-us/azure/azure-monitor/app/correlation) 


