
<properties
pageTitle="VM data appears with delay"
description="VM data appears with delay"
service="microsoft.operationalinsights"
resource="workspaces"
articleId="05738708-090b-4494-8935-c4827de74c53"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32633009"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# VM data appears with delay

The total ingestion time includes:

* Agent time - The time it takes the agent to collect and send a log to Azure Monitor ingestion point.
* Pipeline time - The time for the ingestion pipeline to process the log record.
* Indexing time - The time spent to ingest a log record into Azure Monitor big data store.<br>

## **Recommended Steps**

* Review the [Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) for service availability and issues.
* Review the ingestion aspects and the expected latency for your scenario:<br>

    * [Agent collection latency](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#agent-collection-latency)
    * [Agent upload frequency](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#agent-upload-frequency)
    * [Management solutions data collection](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#management-solutions-collection)
    * [Data process time in pipeline](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#pipeline-process-time)
    * [New custom data types provisioning time](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#new-custom-data-types-provisioning)
    * [Indexing time](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#indexing-time)<br>

* Query your workspace to [measure the ingestion time](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time#checking-ingestion-time)<br>

## **Recommended Documents**

* [Log data ingestion time in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/data-ingestion-time)
* [Azure Monitor Status blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)<br>
