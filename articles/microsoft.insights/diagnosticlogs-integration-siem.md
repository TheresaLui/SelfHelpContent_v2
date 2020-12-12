<properties 
    pageTitle="Integrating Diagnostic settings with 3rd party SIEM tools"
    description="Integrating with SIEM"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="diagnosticlogs-export-siem"
    productPesIds="16875"
    supportTopicIds="32684711"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- Integrating-with-SIEM -->
Platform logs in Azure, including Azure Activity log and resource logs, provide detailed diagnostic and auditing information for Azure resources and the Azure platform they depend on. Platform metrics are collected by default and typically stored in the Azure Monitor metrics database. Platform logs and metrics can be sent to various destinations, including [Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-about), which enable you to stream data to external systems such as third-party SIEMs and other log analytics solutions. The following steps show how to enable platform log export to Event Hub.

## **Recommended Steps**

1. Get familiar with the different [destinations](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#destinations) available, as well as the Destination requirements.
1. Ensure you have the right access requirements to be able to export logs via Event Hub.
1. See this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-in-azure-portal) on how configure diagnostic settings in Azure Portal.
1. See this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-powershell) on how configure diagnostic settings using PowerShell.
1. See this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-azure-cli) on how configure diagnostic settings using Azure CLI.
1. See this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-rest-api) on how configure diagnostic settings using REST API.

## **Recommended Documents**

* [Overview of Azure platform logs](https://docs.microsoft.com/azure/azure-monitor/platform/platform-logs-overview)
* [Overview of Azure resource logs](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs)
* [Complete overview of diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings)
* [Overview of Activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
