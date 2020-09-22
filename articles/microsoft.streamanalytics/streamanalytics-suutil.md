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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Streaming Unit Utilization

Streaming Units (SUs) represent the computing resources that are allocated to execute a job. The higher the number of SUs, the more CPU and memory resources are allocated for your job. This capacity allows you to focus on the query logic and removes the need to manage the hardware to run your Stream Analytics job. To achieve low latency stream processing, Azure Stream Analytics jobs perform all processing in memory. When it is out of memory, the streaming job will fail. As a result, for a production job it’s important to monitor a streaming job’s resource usage and ensure there are enough resources allocated to keep the jobs running 24/7.

There are multiple factors that affect streaming unit utilization. To learn more, see the recommended documents.

## **Recommended Documents**

* [How to use Watermark delay metric to determine performance impact of your jobs?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-set-up-alerts#scenarios-to-monitor)
* [Why did SU% utilization suddenly increase or decrease?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#factors-that-increase-su-utilization)
* [Query parallelization to allow scale and optimize SU % utilization](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parallelization)
* [Understand Event Hub partitions key](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-partitioning#use-of-partition-keys)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
* [Why increasing number of streaming units for a job might not decrease SU % Utilization?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#factors-that-increase-su-utilization)
* [How to fine tuning Cosmos DB output for better performance?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-documentdb-output)
* [How to fine tune Azure SQL DB for better performance?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-sql-output-perf)
