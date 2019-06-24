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
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public,fairfax"
/>

# I can't pick Guest OS namespace and metrics

Virtual machines and virtual machine scale sets have two categories of metrics: **Virtual Machine Host** metrics that are collected by the Azure hosting environment, and **Guest OS** metrics that are collected by the [monitoring agent](https://docs.microsoft.com/azure/azure-monitor/platform/agents-overview) running on your virtual machines. You install the monitoring agent by enabling [Azure Diagnostic Extension](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview).

By default, Guest OS metrics are stored in Azure Storage account, which you pick from the **Diagnostic settings** tab of your resource. If Guest OS metrics aren't collected or metrics explorer cannot access them, you will only see the **Virtual Machine Host** metric namespace:

![metric image](https://docs.microsoft.com/azure/azure-monitor/platform/media/metrics-troubleshoot/cannot-pick-guest-os-namespace.png)

## **Recommended Steps**

 If you don't see **Guest OS** namespace and metrics in metrics explorer:

1. Confirm that [Azure Diagnostic Extension](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-overview) is enabled and configured to collect metrics.
    > [!WARNING]
    > You cannot use [Log Analytics agent](https://docs.microsoft.com/azure/azure-monitor/platform/agents-overview#log-analytics-agent) (also referred to as the Microsoft Monitoring Agent, or "MMA") to send **Guest OS** into a storage account.

1. Verify that storage account isn't protected by the firewall.

1. Use the [Azure storage explorer](https://azure.microsoft.com/features/storage-explorer/) to validate that metrics are flowing into the storage account. If metrics aren't collected, follow the [Azure Diagnostics Extension troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostics-extension-troubleshooting#metric-data-doesnt-appear-in-the-azure-portal).

## **Recommended Documents**

* [Getting started with Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-getting-started)<br>
* [Advanced features of Azure Metrics Explorer](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts)<br>
* [Troubleshooting metrics charts](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-troubleshoot)<br>
* [See a list of available metrics for Azure services](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported)<br>
* [See examples of configured charts](https://docs.microsoft.com/azure/azure-monitor/platform/metric-chart-samples)
