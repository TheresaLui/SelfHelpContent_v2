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
	supportTopicIds="32357236,32628762"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Connectivity
Under some circumstances, you might notice issues with input and output connections. When your job is running, you might see error messages with a yellow triangle near your inputs or outputs on the overview section on Azure portal. These errors are transient by nature and Stream Analytics will keep retrying to self correct. If you notice these errors impacting your job's performance (seen in [watermark delay metric](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-set-up-alerts#scenarios-to-monitor)), you can try restarting the job.

Stream Analytics guarantees no loss of events even when you see these transient errors. When starting a job, you can choose 'when last stopped' to resume processing from where you last left.

If you are having issues connecting to reference data, please check if the [ath pattern of blob](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-use-reference-data#configure-blob-reference-data) correct. If this incorrect, the job will indefinitely wait till a blob becomes available in the specified path. If you are using Azure SQL database as reference data and having issues connecting to it, you can try [esting the connection to this input source](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input#input-events-not-received-by-job)

If this or other issues persists, you can learn how to troubleshoot by reading these recommended documents.

## **Recommended Documents**

* [Configuring streaming input](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-inputs)
* [Configuring reference data input](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-use-reference-data)
* [Configuring output](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-outputs)
* [Troubleshoot input connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-input)
* [Troubleshoot output connections](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-output)
* [Troubleshoot using metrics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-job-diagram-with-metrics#troubleshoot-by-using-metrics)
