<properties
	pageTitle="Malformed input events causes deserialization errors"
	description="Malformed input events causes deserialization errors"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-deserializationerror"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628778"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Malformed Input Event Causes Deserialization Errors

Deserialization issues are caused when the input stream of your Stream Analytics job contains malformed messages.To address this issue, see the recommended documents.

Note that Stream Analytics cannot process Event Hub Capture files from blob storage even though it is in AVRO format. Doing so will result in deserialization errors.

## **Recommended Documents**

* [Deserialization errors caused by malformed input events](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#malformed-input-events-causes-deserialization-errors)<br>
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
