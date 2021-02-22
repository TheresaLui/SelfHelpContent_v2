<properties 
    pageTitle="Using Diagnostic settings to export to Log Analytics"
    description="Integrating with Log Analytics"
    service="microsoft.insights"
    resource=""
    authors="shilpasharmaAM"
    ms.author="shilsha"
    selfHelpType="generic"
    articleId="diagnosticlogs-export-loganalytics"
    productPesIds="16875"
    supportTopicIds="32684712"
    cloudEnvironments="public, Fairfax, usnat, ussec"
     ownershipId="AzureMonitoring_AzureMetrics"
/>

# <-- Integrating-with-Log Analytics -->
Platform logs in Azure, including Azure Activity log and resource logs, provide detailed diagnostic and auditing information for Azure resources and the Azure platform they depend on.  Platform metrics are collected by default and typically stored in the Azure Monitor metrics database. Platform logs and metrics can be sent to various destinations, including [Log Analytics](https://docs.microsoft.com/azure/azure-monitor/log-query/log-query-overview). Following steps will walk you through how to enable platform log export to Log Analytics.

## **Recommended Steps**

1. Familiarize with the different [destinations](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#destinations) available as well as the Destination requirements, in this case creating the Log Analytics Workspace.
1. Refer to this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-in-azure-portal) on how configure diagnostic settings in Azure Portal.
1. Refer to this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-powershell) on how configure diagnostic settings using PowerShell.
1. Refer to this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-azure-cli) on how configure diagnostic settings using Azure CLI.
1. Refer to this [guide](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings#create-using-rest-api) on how configure diagnostic settings using REST API.

## **Recommended Documents**

* [Overview of Azure platform logs](https://docs.microsoft.com/azure/azure-monitor/platform/platform-logs-overview)
* [Overview of Azure resource logs](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs)
* [Complete overview of diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings)
* [Overview of Activity log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log)
* [Stream Azure monitoring data to an event hub](https://docs.microsoft.com/azure/azure-monitor/platform/stream-monitoring-data-event-hubs)
