<properties
	pageTitle="Job started to fail with error"
	description="Job started to fail with error"
	service="Microsoft.DataLakeAnalytics"
	resource="datalake"
	ms.author="guyhay"
	authoralias="guyhay"
	authors="guyhay"
	selfHelpType="resource"
	supportTopicIds="32680650"
	resourceTags=""
	productPesIds="15940"
	cloudEnvironments="public"
	articleId="datalakeanalytics-job-started-to-fail-with-error"
/>

# U-SQL jobs failing

U-SQL jobs can fail for a number of reasons.  Common reasons include 

* Transient outages of the services such as DNS, Networking, ADLS that ADLA depends on
* Changes to the ACLs of the ADLS files consumed in the job
* Changing data sizes, which may cause data skew or storage throttling
* Changing data-distribution across partitions, which may cause errors or un-optimized execution of jobs
* Improvements to the U-SQL compiler and optimizer which may cause existing old optimizer hints to become outdated 
* Note that jobs that fail with error type "SYSTEM" are not charged 


## **Recommended Steps**

1. Check if there are outages in the region where this job is running (https://status.azure.com/status)<br>
2. Understand what the error what caused the error by using the Job Browser in Visual Studio or the Azure Portal<br>

## **Recommended Documents**

* [Use Job Browser and Job View for Azure Data Lake Analytics](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-view-jobs)<br>
* [Monitor jobs in Azure Data Lake Analytics using the Azure Portal](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-monitor-and-troubleshoot-jobs-tutorial)<br>
* [Azure Data Lake Analytics pricing FAQ](https://azure.microsoft.com/pricing/details/data-lake-analytics/)<br>
* [ADLS Gen1 - Best practices for using Azure Data Lake Store Gen1](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices)<br>
* [ADLS Gen1 - Performance and scale considerations](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices#performance-and-scale-considerations)<br>
* [Diagnose ADLS Gen1 throttling errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError/)<br>
* [Diagnose ADLS Gen1 timeout errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError/)<br>
