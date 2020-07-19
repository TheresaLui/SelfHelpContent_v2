<properties
	pageTitle="StreamAnalyticsJobFailedToStartTsg"
	description="Stream Analytics failed to start."
	infoBubbleText="Your Stream Analytics job has been configured incorrectly. Please see details on the right."
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidram"
	ms.author="sidram"
	displayOrder=""
	articleId="StreamAnalyticsNoInputTsg"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32628786,32357228"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_StreamAnalytics"
/>

# Stream Analytics is not receiving any input

## Stream Analytics job is not receiving any input
<!--issueDescription-->
It was found that your Stream Analytics job  is not receiving any input from the configured input sources. This could happen due to misconfigured start time, or problems with connectivity to your input.
<!--/issueDescription-->


## **Recommended Steps**

1. Make sure when you start your Stream Analytics job, you select the right Start Time
2. [Test connection](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#input-events-not-received-by-job) of job with the input and sample data to see if event stream is flowing in as expected. If there is no data while sampling, please check that your device or application is sending events to your input source as expected.


## **Recommended Documents**

* [Test input and output connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#input-events-not-received-by-job)
