<properties
    pageTitle="I can't find my resource to select it in metrics explorer"
    description="I can't find my resource to select it in metrics explorer"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="1"
    articleId="metrics-cant-find-your-resource-to-select-it"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677614"
    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-cant-find-your-resource-to-select-it -->

## I can't find my resource to select it in metrics explorer

You clicked on the **Select a resource** button, but don't see your resource in the resource picker dialog.

## **Recommended Steps**

Metrics explorer requires you to select subscriptions and resource groups before listing available resources. If you don't see your resource:

* Ensure that you've selected correct subscription in the **Subscription** dropdown. If your subscription isn't listed, click on the  **Directory + Subscription settings** and add a subscription with your resource.
* Ensure that you've selected the correct resource group. **NOTE**: For best performance, when you first open metrics explorer, the **Resource group** dropdown has no pre-selected resource groups. You must pick at least one group before you can see any resources.

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
