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

## **Recommended Steps**

### 1. **Grouped under a category say HTTP** 

* Sometimes the dependency is grouped as an external dependency and gets grouped under the category typically http. When you expand that category, you will be able to see it.
* To avoid this, ensure you have instrumented your app components using a supported SDK. Refer [to this article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs.


### 2. **Select a longer time range** 

* Increase the time duration on the map to check if the component appears as it may not have been called in the last hour but might appear for a longer duration selected.


### 3. **App components is showing as an external dependency**  

* If the app component is showing as an external dependency (like **correlation** component in the map) then either you don’t have [permissions](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control#to-provide-access-to-another-user) to the app resource or you need to instrument the app component by using the [supported SDKs](https://docs.microsoft.com/azure/application-insights/app-insights-platforms). 

### 4. **Check Auto collected dependency**

* If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.microsoft.com/azure/application-insights/auto-collect-dependencies). If not, you can still track it manually with a [track dependency call](https://docs.microsoft.com/azure/application-insights/app-insights-api-custom-events-metrics#trackdependency).

### 5. **Update Map Component**

* Check to see if the **update map components** button is failing to light up. This may happen for very large distributed applications. Reducing the time range you are querying for may help here.

## **Recommended Documents**

* [Troubleshooting Application Map](https://docs.microsoft.com/azure/azure-monitor/app/app-map#troubleshooting)
* [Telemetry correlation](https://docs.microsoft.com/azure/azure-monitor/app/correlation) 


