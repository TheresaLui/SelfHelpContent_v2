<properties 
    pageTitle="How do I troubleshoot the Application Map?"
    description="Explain how to configure the Application Map"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights-appmap-mooncake"
    displayOrder="3"
    selfHelpType="resource"
    cloudEnvironments="MoonCake"
    productPesIds="" 
    supportTopicIds=""
 	ownershipId="ASEP_ContentService_Placeholder"
/>
 
# How do I troubleshoot the Application Map?

## **Recommended Steps**

1. Make sure you're using an officially supported SDK. Unsupported/community SDKs might not support correlation. Refer to [this article](https://docs.azure.cn/azure-monitor/app/platforms) for a list of supported SDKs.
2. Upgrade all components to the latest SDK version
3. If you're using Azure Functions with C#, upgrade to [Functions V2](https://docs.azure.cn/azure-functions/functions-versions)
4. Confirm [cloud_RoleName](https://docs.azure.cn/azure-monitor/app/app-map#Set-cloud-RoleName) is correctly configured
5. If you're missing a dependency, make sure it's in the list of [auto-collected dependencies](https://docs.azure.cn/azure-monitor/app/auto-collect-dependencies). If not, you can still track it manually with a [track dependency call](https://docs.azure.cn/azure-monitor/app/api-custom-events-metrics#trackdependency).

## **Recommended Documents**

* [Application Map](https://docs.azure.cn/azure-monitor/app/app-map)
