<properties
	pageTitle="Billing and Pricing"
	description="Billing and Pricing"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-billing-pricing"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32628958"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Billing and Pricing Information
Azure Stream Analytics is priced by the number of streaming units (SUs) required to process the data into the service. Each streaming unit providing is billed on an hourly basis. 

Once the SUs are allocated and job is started, you will be charged according to the pricing mode. There can be idle states where the job is running but not processing any data. Billing will still occur in these cases as your job has some amount of compute and memory resources allocated in the form of SUs.

To learn more about pricing in Azure Stream Analytics, see the recommended documents.

## **Recommended Documents**

* [Azure Stream Analytics pricing](https://azure.microsoft.com/pricing/details/stream-analytics/)
* [How many SUs are required for a job?](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-streaming-unit-consumption#how-many-sus-are-required-for-a-job)
* [Calculate maximum streaming units for a job](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-parallelization#calculate-the-maximum-streaming-units-of-a-job)
