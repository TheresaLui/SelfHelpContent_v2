<properties
	pageTitle="Stream Analytics Job output sink is potentially slow"
	description="Stream Analytics Job output sink is potentially slow"
	infoBubbleText="Your Stream Analytics Job output sink is potentially slow. Please see details on the right."
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidram"
	ms.author="sidram"
	displayOrder=""
	articleId="StreamAnalyticsDataErrorsTsg"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32628786,32357228"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_StreamAnalytics"
/>

# Stream Analytics Job output sink is potentially slow

## Stream Analytics Job output sink is slow
<!--issueDescription-->
It was found that writing to one of your outputs is slow. This can increase watermark delay and backlog for this output and other outputs that share the same input. 

If there are throttling errors from downstream sink, please consider if the sink can be configured to support additional throughput. This might involve SKU change. If there are no throttling errors, consider partitioning and then scaling out Stream Analytics job.
<!--/issueDescription-->


## **Recommended Steps**

* [Partitioning and scaling out your job](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-scale-jobs)
