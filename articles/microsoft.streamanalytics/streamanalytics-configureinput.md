<properties
	pageTitle="Configure input"
	description="Configure input"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-configureinput"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628768"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Configure Input

Inputs are divided into two types: data stream inputs and reference data inputs. 

Stream Analytics jobs must include at least one data stream input. Event Hubs, IoT Hub, and Blob storage are supported as data stream input sources.

Reference data is a static or slowly changing dataset in Blob Store or Azure SQL Database that can be joined with stream input. You cannot create and run a Stream Analytics job with reference data input alone. 

At this time, Stream Analytics does not support VNET and therefore your jobs cannot connect to any input or output resources that are behind a firewall or in a VNET. We are working on adding [support for VNET](https://feedback.azure.com/forums/270577-stream-analytics/suggestions/34846942-stream-analytics-vnet-support) and will become available in the coming months.

To learn more about configuring inputs in Azure Stream Analytics job, see the recommended documents.


## **Recommended Documents**
* [Maximum number of inputs in a job](https://docs.microsoft.com/azure/azure-subscription-service-limits#stream-analytics-limits)
* [Different types of streaming data input](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-inputs)
* [Different types of reference data input](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-use-reference-data)
* [How to use Azure SQL DB as reference data input](https://docs.microsoft.com/azure/stream-analytics/sql-reference-data)
* [Azure SQL DB reference data input FAQs](https://docs.microsoft.com/azure/stream-analytics/sql-reference-data#faqs)
* [How to parse array and record data types in JSON and AVRO](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parsing-json)
