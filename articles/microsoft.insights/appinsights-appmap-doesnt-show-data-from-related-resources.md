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

![appmap image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/app-insights/application-map-not-showing-data-from-related-resources.png)

## **Recommended Steps**

### 1. **Permissions**

* If Y and Z are in a different Application Insights resource and you don’t see data related to them then ensure that that you have [permissions](https://docs.microsoft.com/azure/azure-monitor/app/resources-roles-access-control#to-provide-access-to-another-user) to these different App Insights resource. 

### 2. **Using the supported SDK to instrument**  

* Make sure you have instrumented the components using supported SDKs. The component will not show any data if its not instrumented. Refer to this [article](https://docs.microsoft.com/azure/application-insights/app-insights-platforms) for a list of supported SDKs. Also, confirm [cloud_RoleName](https://docs.microsoft.com/azure/azure-monitor/app/app-map#Set-cloud-RoleName) is correctly configured for Y or Z.

### 3. **If Y or Z are application components in a different Application Insights resource:**

* Check to see if the **update map components** button is failing to light up. This may happen for very large distributed applications. Reducing the time range you are querying for may help here.
* If you don’t see Z (direct HTTP calls):
    * Upgrade all components to the latest SDK version
    * If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* If you don’t see Y (async across a queue): 
    * Click on *Try* button on the purple banner on the top to try preview of App Map that provides this cross-component tracing across supported queues only. Note: This is a preview version only. 

## **Recommended Documents**

* [Application Map Troubleshooting](https://docs.microsoft.com/azure/azure-monitor/app/app-map#troubleshooting)