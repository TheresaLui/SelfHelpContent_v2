<properties
    pageTitle="I can't pick Guest OS namespace and metrics"
    description="I can't pick Guest OS namespace and metrics"
    service="microsoft.insights"
    resource="components"
    authors="vgorbenko"
    ms.author="vitalyg"
    displayOrder="6"
    articleId="metrics-cannot-pick-guest-os-namespace-and-metrics"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32677615,32684744,32684736,32684737,32684738,32684739,32684740,32684746,32684747,32684757"

    resourceTags=""
    productPesIds="16250"
    cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
/>

# <-- metrics-cannot-pick-guest-os-namespace-and-metrics -->

## Use this information if you can't pick Guest OS metrics in Azure Metrics Explorer or having troubles collecting metrics on computers running Windows or Linux

Virtual machines and virtual machine scale sets have two categories of metrics: **Virtual Machine Host** metrics that are collected by the Azure hosting environment, and **Guest OS (classic)** metrics that are collected by the [monitoring agent](https://docs.microsoft.com/azure/azure-monitor/platform/agents-overview) running on your virtual machines. You install the monitoring agent by enabling [Azure Diagnostic Extension](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview).

| **What is the best way to enable collection of Guest OS Metrics?** |
|----------------------------------------------------------------|
|If you enable monitoring on the **Diagnostic Settings** tab of your Virtual Machine, you can select performance counter that will be saved in a storage account, and appear under **Guest (Classic)** metric [namespace in Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot#cannot-pick-guest-os-namespace-and-metrics). This method has limitations and is no longer a recommended way of charting or alerting on Virtual Machine Guest OS metrics. For the recommended method of collecting guest OS metrics, see the documentation for [Windows VMs](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-windows-install) or [Linux VMs](https://docs.microsoft.com/azure/azure-monitor/platform/collect-custom-metrics-linux-telegraf).|

**If you are using Guest OS (classic) metrics:** By default, Guest OS metrics are stored in Azure Storage account, which you pick from the **Diagnostic settings** tab of your resource. If Guest OS metrics aren't collected or metrics explorer cannot access them, you will only see the **Virtual Machine Host** metric namespace:

![metric image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/cannot-pick-guest-os-namespace.png)

## **Recommended Steps**

 If you don't see **Guest OS** namespace and metrics in metrics explorer:

* Confirm that [Azure Diagnostic Extension](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview) is enabled and configured to collect metrics. NOTE: You cannot use [Log Analytics agent](https://docs.microsoft.com/azure/azure-monitor/platform/agents-overview#log-analytics-agent) (also referred to as the Microsoft Monitoring Agent, or "MMA") to send **Guest OS** into a storage account.
* Ensure that **Microsoft.Insights** resource provider is [registered for your subscription](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot#microsoftinsights-resource-provider-isnt-registered-for-your-subscription)
* Verify that storage account isn't protected by the firewall. Azure portal needs access to storage account in order to retrieve metrics data and plot the charts.
* Use the [Azure storage explorer](https://azure.microsoft.com/features/storage-explorer/) to validate that metrics are flowing into the storage account. If metrics aren't collected, follow the [Azure Diagnostics Extension troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-troubleshooting#metric-data-doesnt-appear-in-the-azure-portal).

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
