<properties
	pageTitle="Degraded state"
	description="Degraded state"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-degraded"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628782"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public"
	ms.author="sidram"
/>

# Degraded state

A job enters a degraded state due to transient issues. This could be due to network connectivity or availability of other Azure services the job is connected to. Stream Analytics automatically tries to recover from such transient errors. When the job is in a degraded state, the performance of the job could be impacted.

It is recommended to wait to see if the job automatically recovers. If the job is in degraded state for a long period of time or ends up in a failed state, you can learn the root cause by looking at the activity logs.

To learn more, see the recommended document.

## **Recommended Document**

* [Debug using activity logs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagnostic-logs#debugging-using-activity-logs)
