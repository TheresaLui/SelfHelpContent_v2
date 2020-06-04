<properties
	pageTitle="High Resource Utilization"
	description="Utilization of Stream Analytics job is high."
	infoBubbleText="Your Stream Analytics job has found to have high resource utilization. See details on the right."
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidram"
	ms.author="sidram"
	displayOrder=""
	articleId="streamanalyticsjobscaleouttsg"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32628786,32357228"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_StreamAnalytics"
/>

# High Streaming job resource utilization

## Stream Analytics job has high resource utilization
<!--issueDescription-->
It was found that your Stream Analytics job has high resource utilization. Every job has some amount of memory and compute power that is used to process incoming events. High resource utilization might impact job's performance, therefore, it is recommended that you increase the number of Streaming Units assigned to a job.
<!--/issueDescription-->


## **Recommended Steps**

1. Check the watermark delay metric by going to Metrics under the Monitoring section of your Stream Analytics job on portal
2. If the watermark delay metric is acceptable (in the order of seconds) and has not steadily increased over time, you can choose to continue to run the job without any changes. However, if there is a spike in the number of incoming events, your job's performance may be impacted.
3. You can also learn which parts of your query can cause high resource utilization and try to optimize your query
4. Increase the number of Streaming Units assigned to your job by going to Scale under Configure section on portal

## **Recommended Documents**

* [Why did SU% utilization suddenly increase or decrease?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#factors-that-increase-su-utilization)
