<properties
	pageTitle="SU Util"
	description="SU Util"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-suutil"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628786,32357228"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public"
	ms.author="sidram"
/>

# Streaming Units Utilities
Streaming Units (SUs) represent the computing resources that are allocated to execute a job. The higher the number of SUs, the more CPU and memory resources are allocated for your job. This capacity allows you to focus on the query logic and removes the need to manage the hardware to run your Stream Analytics job. To achieve low latency stream processing, Azure Stream Analytics jobs perform all processing in memory. When it is out of memory, the streaming job will fail. As a result, for a production job it’s important to monitor a streaming job’s resource usage and ensure there are enough resources allocated to keep the jobs running 24/7.

There are multiple factors that affect streaming unit utilization. To learn more, see the recommended documents.

## **Recommended Documents**

* [Use watermark delay metric to check performance of your job](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-set-up-alerts#scenarios-to-monitor)
* [Why did SU% utilization suddenly increase or decrease?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#factors-that-increase-su-utilization)
* [Query parallelization to optimize SU % utilization](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parallelization)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
