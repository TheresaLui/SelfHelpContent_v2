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
	cloudEnvironments="public"
	ms.author="sidram"
/>

# Configure Input

Inputs are divided into two types: data stream inputs and reference data inputs. 

Stream Analytics jobs must include at least one data stream input. Event Hubs, IoT Hub, and Blob storage are supported as data stream input sources.

Reference data is a static or slowly changing dataset in Blob Store or Azure SQL Database that can be joined with stream input. You cannot create and run a Stream Analytics job with reference data input alone. 

To learn more about configuring inputs in Azure Stream Analytics job, see the recommended documents.


## **Recommended Documents**

* [Different types of streaming input](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-inputs)
* [Configuring reference data](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-use-reference-data)
* [How to parse array and record data types](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parsing-json)
