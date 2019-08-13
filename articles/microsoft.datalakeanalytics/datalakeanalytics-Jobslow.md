<properties
	pageTitle="Job started to run slow"
	description="Job started to run slow"
	service="Microsoft.DataLakeAnalytics"
	resource="datalake"
	ms.author="guyhay"
	authoralias="guyhay"
	authors="guyhay"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32680652"
	resourceTags=""
	productPesIds="15940"
	cloudEnvironments="public"
	articleId="datalakeanalytics-job-started-to-run-slow"
/>

# U-SQL jobs started to run slow

U-SQL jobs can run slowly for a number of reasons.  Common reasons include 

* Transient outages of the services such as DNS, Networking, ADLS that ADLA depends on
* Changing data sizes, which may cause data skew or storage throttling
* Chaging data-distribution across partitions, which may cause errors or un-optimized execution of jobs
* Improvements to the U-SQL compiler and optimiser which may cause existing old optimiser hints to become outdated 

## **Recommended Documents**

* [ADLA - Resolve data-skew problems by using Azure Data Lake Tools for Visual Studio] (https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-data-skew-solutions)<br>
* [ADLA - Troubleshoot an abnormal recurring job] (https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-debug-recurring-job)<br>
* [ADLS Gen1 - Best practicies for using Azure Data Lake Store Gen1] (https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices)<br>
* [ADLS Gen1 - Performance and scale considerations] (https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices#performance-and-scale-considerations)<br>
* [Diagnose ADLS Gen1 throttling errors] (https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError/)<br>