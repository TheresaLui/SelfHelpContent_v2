<properties
    pageTitle="V2 - Monitor and Metrics Common Solutions"
    description="V2 - Monitor and Metrics Common Solutions"
    service=""
    resource=""
    authors="chez-charlie"
    ms.author="chez"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629510, 32637164"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8c727d6a-a637-4401-a801-cafb122d252c"
	ownershipId="AzureData_DataFactory"
/>

# V2 - Monitor and Metrics Common Solutions

## **Recommended Steps**

1. Data Factory stores pipeline run information for 45 days only. If users want to persist the log for longer period, they may [Send Logs to Azure Monitor and Log Analytics](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor) or [Query and Capture Diagnostic Logs with SDK](https://docs.microsoft.com/azure/data-factory/monitor-programmatically).

1. __Notes__ on Azure Data Factory - Log Analytics integration: <br>

    1. There is [a known limitation in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/resource-logs-collect-workspace#known-limitation-column-limit-in-azurediagnostics) that a log table cannot have more than 500 columns <br>
    1. To address any problems with Log Analytics, we _strongly_ recommend users [configure diagnostic settings](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#configure-diagnostic-settings-and-workspace) to _Resource-Specific_ mode instead of _Azure-Diagnostics_ mode

1. __Notes__ on Log Analytics tables: <br>

    * In _Resource-Specific_ mode, diagnostic logs from Azure Data Factory flow into _ADFPipelineRun_, _ADFTriggerRun_ and _ADFActivityRun_ tables <br>
    * In _Azure-Diagnostics_ mode, diagnostic logs flow into _AzureDiagnostics_ table <br>
    * If you recently deploys _Azure Data Factory Analytics (Preview)_ from market place, the solution uses _Resource-Specific_ mode

## **Recommended Documents**

* Monitor visually [Document](https://docs.microsoft.com/azure/data-factory/monitor-visually), including following sections: <br>

  * [Monitor Pipelines](https://docs.microsoft.com/azure/data-factory/monitor-visually#select-a-data-factory-to-monitor) <br>
  * [Promote User Properties to Monitor](https://docs.microsoft.com/azure/data-factory/monitor-visually#promote-user-properties-to-monitor) <br>
  * [Gantt Views](https://docs.microsoft.com/azure/data-factory/monitor-visually#gantt-views) <br>
  * [Alerts](https://docs.microsoft.com/azure/data-factory/monitor-visually#alerts) <br>

* Monitor with Azure Monitor [Document](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor), including following sections <br>

  * [Logs and Event Schema](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#schema-of-logs-and-events) <br>
  * [Metrics](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#metrics) <br>
  * [Integration with Azure Monitor and Log Analytics](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#monitor-data-factory-metrics-with-azure-monitor) <br>
  * [Alerts](https://docs.microsoft.com/azure/data-factory/monitor-using-azure-monitor#alerts) <br>

* Monitor with Software Development Kits (SDKs) [Document](https://docs.microsoft.com/azure/data-factory/monitor-programmatically) <br>

**FAQ**

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions) <br>
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
