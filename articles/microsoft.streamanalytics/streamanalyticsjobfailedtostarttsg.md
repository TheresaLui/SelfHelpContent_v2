<properties
	pageTitle="Job failed to start"
	description="Stream Analytics failed to start."
	infoBubbleText="Your Stream Analytics job has been configured incorrectly. Please see details on the right."
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidram"
	ms.author="sidram"
	displayOrder=""
	articleId="StreamAnalyticsJobFailedToStartTsg"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32628786,32357228"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_StreamAnalytics"
/>

# Stream Analytics failed to start

## Stream Analytics job failed to start
<!--issueDescription-->
It was found that your Stream Analytics job failed to start due to incorrect job configuration. This could arise due to incorrectly configured inputs or output. It could also be caused if the Stream Analytics query is incorrect.
<!--/issueDescription-->

## **Recommended Steps**

1. Make sure your job has at least one stream input and at least one supported output
2. Check if the all inputs and outputs are configured correctly using [test connection](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#input-events-not-received-by-job)
3. Check [logs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagnostic-logs#debugging-using-activity-logs) to see what is causing your job to fail
4. Use Stream Analytics query language reference to make sure your query is valid

## **Recommended Documents**

* [Test input and output connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#input-events-not-received-by-job)
* [Debug using activity logs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagnostic-logs#debugging-using-activity-logs)
