<properties
	pageTitle="Delayed output"
	description="Delayed output"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-delayedoutput"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628780"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Delayed Output
When a Stream Analytics job is started, the input events are read, but there can be a delay in the output being produced in certain scenarios.

It is important to ensure data is getting ingested into all partitions of your Event Hubs or IoT Hub. When one input partition is not receiving input, this can lead to a 5 second delay of your output.

If your job is processing events by Arrival Time (using TIMESTAMP BY clause in your query), your [event ordering policies](https://docs.microsoft.com/azure/stream-analytics/event-ordering) could also delay the output produced. When configuring these settings, it is important to remember prioritize your data correctness and latency requirements.

There are scenarios in which your output might be delayed. To learn more, see the recommended documents.

## **Recommended Documents**

* [Job output is delayed](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-output#job-output-is-delayed)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
