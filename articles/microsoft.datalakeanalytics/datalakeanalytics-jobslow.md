<properties
	pageTitle="Job started to run slow"
	description="Job started to run slow"
	service="Microsoft.DataLakeAnalytics"
	resource="accounts"
	ms.author="guyhay"
	authoralias="guyhay"
	authors="guyhay"
	displayOrder="12"
	selfHelpType="resource"
	supportTopicIds="32680652"
	resourceTags=""
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="datalakeanalytics-job-started-to-run-slow"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>

# U-SQL jobs started to run slow

U-SQL jobs can run slowly for a number of reasons.  Common reasons include: 

* Transient outages of the services such as DNS, Networking, ADLS that ADLA depends on
* Changing data sizes may cause data skew or storage throttling
* Changing data-distribution across partitions may cause errors or un-optimized execution of jobs
* Incorrect Azure Data Lake Analytics compute resources (AUs assigned to the job, AU quota assigned to the ADLA account, or queued jobs)
* Improvements to the U-SQL compiler and optimizer may cause existing optimizer hints to become outdated 

## **Recommended Steps**

1. Check if there are outages in the region where this job is running on [Azure status page](https://status.azure.com/status)<br>
2. Understand the error that caused the job to fail by using the either the Job Browser in Visual Studio or the Job management tab for the ADLA account in the Azure Portal<br>

## **Recommended Documents**

* [ADLA - Resolve data-skew problems by using Azure Data Lake Tools for Visual Studio](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-data-skew-solutions)<br>
* [ADLA - Troubleshoot an abnormal recurring job](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-debug-recurring-job)<br>
* [ADLA - Learn about managing your compute resources, account-level policies, and job-level policies](https://blogs.msdn.microsoft.com/azuredatalake/2017/06/08/managing-your-azure-data-lake-analytics-compute-resources-overview/)<br>]
* [ADLS Gen1 - Best practices for using Azure Data Lake Store Gen1](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices)<br>
* [ADLS Gen1 - Performance and scale considerations](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices#performance-and-scale-considerations)<br>
* [Diagnose ADLS Gen1 throttling errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError/)<br>
