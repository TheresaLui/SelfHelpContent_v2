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
	supportTopicIds="32628786"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public"
	authorAlias="sidram"
/>

# SU Util
Streaming Units (SUs) represents the computing resources that are allocated to execute a job. The higher the number of SUs, the more CPU and memory resources are allocated for your job. This capacity lets you focus on the query logic and abstracts the need to manage the hardware to run your Stream Analytics job in a timely manner. To achieve low latency stream processing, Azure Stream Analytics jobs perform all processing in memory. When running out of memory, the streaming job fails. As a result, for a production job, it’s important to monitor a streaming job’s resource usage, and make sure there is enough resource allocated to keep the jobs running 24/7.

There are multiple factors that affect streaming unit utilization. To learn more, see the following documentation:


## **Recommended documents**

[Factors that increase SU% utilization](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#factors-that-increase-su-utilization)<br>
[Query parallelization to optimize SU % utilization](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parallelization)<br>
[Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)