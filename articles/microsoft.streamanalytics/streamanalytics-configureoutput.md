<properties
	pageTitle="Configure output"
	description="Configure output"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-configureoutput"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628769"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Configure Output
You can store or direct the results of a Stream Analytics job to many destinations like SQL database, Cosmos DB, Power BI, Azure Functions, and more. 

It is important to make sure your Stream Analytics job has permissions to write to output sinks. Lack of enough permissions will cause problems writing results to output. 

At this time, Stream Analytics does not support VNET and therefore your jobs cannot connect to any input or output resources that are behind a firewall or in a VNET. We are working on adding [support for VNET](https://feedback.azure.com/forums/270577-stream-analytics/suggestions/34846942-stream-analytics-vnet-support) and will become available in the coming months.

To learn more about configuring outputs in Azure Stream Analytics job, see the recommended documents.

## **Recommended Documents**

* [Maximum number of outputs in a job](https://docs.microsoft.com/azure/azure-subscription-service-limits#stream-analytics-limits)
* [Output types for a job](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-outputs)
* [Fine tuning Cosmos DB output for better performance](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-documentdb-output)
* [How to achieve better write throughput when using SQL Azure Database](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-sql-output-perf)
* [Prevent duplicate entries when writing to SQL Azure Database](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-troubleshoot-output#key-violation-warning-with-azure-sql-database-output)
* [Authenticate to ADLS Gen1 with managed identities](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-managed-identities-adls)
