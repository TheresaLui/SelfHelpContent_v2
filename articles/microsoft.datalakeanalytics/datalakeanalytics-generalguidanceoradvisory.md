<properties
	pageTitle="General guidance or advisory"
	description="General guidance or advisory"
	service="Microsoft.DataLakeAnalytics"
	resource="accounts"
	ms.author="guyhay"
	authoralias="guyhay"
	authors="guyhay"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32680880"
	resourceTags=""
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="datalakeanalytics-general-guidance-or-advisory"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>

# General guidance or advisory
The top three support incident types that customers create support tickets for ADLA are:

* Difficulties using the Azure Portal 
* A U-SQL job failed
* Errors submitting a U-SQL job

## **Recommended Steps**

1. Check if there are outages in the region where this job is running on [Azure status page](https://status.azure.com/status)<br>
2. Understand the error that caused the job to fail by using the Job Browser in Visual Studio or the Job management tab for the ADLA account in the Azure Portal<br>

## **Recommended Documents**

* [Develop U-SQL scripts by using Data Lake Tools for Visual Studio](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-get-started)<br>
* [Use Job Browser and Job View for Azure Data Lake Analytics](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-view-jobs)<br>
* [Monitor jobs in Azure Data Lake Analytics using the Azure Portal](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-monitor-and-troubleshoot-jobs-tutorial)<br>
* [Resolve data-skew problems by using Azure Data Lake Tools for Visual Studio](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-data-skew-solutions)<br>
* [Diagnose ADLS Gen1 throttling errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError/)<br>
* [Diagnose ADLS Gen1 timeout errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError/)<br>