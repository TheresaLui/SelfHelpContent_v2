<properties
	pageTitle="connectivity"
	description="connectivity"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-connectivity"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32357236,32628762,32357226"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public"
	ms.author="sidram"
/>

# Connectivity
Under some circumstances, you might notice issues with input and output connections. When your job is running, you might see error messages with a yellow triangle near your inputs or outputs on the overview section on Azure portal. These errors are transient by nature and Stream Analytics will keep retrying to self correct. If you notice these errors impacting your job's performance (seen in [watermark delay metric](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-set-up-alerts#scenarios-to-monitor)), you can try restarting the job.

If this or other issues persists, you can learn how to troubleshoot by reading these recommended documents.

## **Recommended Documents**

* [Troubleshoot input connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input)
* [Troubleshoot output connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-output)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
