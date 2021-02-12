<properties
	pageTitle="Error in Portal"
	description="Error in Portal"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-errorportal"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628757, 32628785"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Error in Portal
Errors that you see on the Azure portal could be transient in nature. Stream Analytics will automatically retry and try to recover from such errors. Other errors can result in job failures. Failures can be caused by an unexpected query result, by connectivity to devices, or by an unexpected service outage. The activity and diagnostics logs in Stream Analytics can help you identify the cause of issues.

Stream Analytics guarantees at-least-once delivery of events. Even if your job stops due to an error, you have the ability to start your job 'when last stopped'. 

## **Recommended Documents**

* [Understanding and dealing with input and output data errors](https://docs.microsoft.com/azure/stream-analytics/data-errors)
* [Debug using activity logs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagnostic-logs#debugging-using-activity-logs)
* [Debug using diagnostic logs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagnostic-logs#send-diagnostics-to-log-analytics)
* [How does Stream Analytics handle errors and retries when writing to Azure Functions?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-with-azure-functions#error-handling-and-retries)
* [Is a known Azure outage impacting your job?](https://azure.microsoft.com/status/)
* [My job failed due to a runtime error. Is my data lost?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-introduction#reliability)
* [Understanding error codes to help debug unexpected behaviors](https://docs.microsoft.com/azure/stream-analytics/configuration-error-codes)
