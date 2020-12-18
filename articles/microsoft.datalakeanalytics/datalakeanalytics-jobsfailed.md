<properties
  pagetitle="U-SQL jobs failing&#xD;"
  service="microsoft.datalakeanalytics"
  resource="accounts"
  ms.author="guyhay,xujiang1"
  selfhelptype="Resource"
  supporttopicids="32680650"
  resourcetags=""
  productpesids="15940"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="datalakeanalytics-job-started-to-fail-with-error"
  ownershipid="AzureData_AzureDataLakeAnalytics" />
# U-SQL jobs failing

U-SQL jobs can fail for a number of reasons.  Common reasons include:

* Transient outages of the services such as DNS, networking, ADLS that ADLA depends on
* Changes to the ACLs of the ADLS files consumed in the job
* Changing data size that causes data skew or storage throttling
* Changing data-distribution across partitions that causes errors or unoptimized execution of U-SQL jobs
* Too many table INSERTS without periodic ALTER TABLE REBUILD. [Alter table](https://docs.microsoft.com/u-sql/ddl/tables/alter-table) can lead to job degradation and failure
* Outputting huge amount of data to a single file
* Improvements to the U-SQL compiler and optimizer that can cause existing optimizer hints to become outdated

**Note:** U-SQL jobs that fail with error type "SYSTEM" are not charged.

## **Recommended Steps**

1. Check if there are outages in the region where this job is running on the [Azure status page](https://status.azure.com/status)<br>
2. Find the error that caused the job to fail by using the Job Browser in Visual Studio, or the Job management tab for the ADLA account in the Azure portal<br>

## **Recommended Documents**

* [Use Job Browser and Job View for Azure Data Lake Analytics](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-data-lake-tools-view-jobs)<br>
* [Monitor U-SQL jobs in Azure Data Lake Analytics using the Azure portal](https://docs.microsoft.com/azure/data-lake-analytics/data-lake-analytics-monitor-and-troubleshoot-jobs-tutorial)<br>
* [Azure Data Lake Analytics pricing FAQ](https://azure.microsoft.com/pricing/details/data-lake-analytics/)<br>
* [ADLS Gen1 - Best practices for using Azure Data Lake Store Gen1](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices)<br>
* [ADLS Gen1 - Performance and scale considerations](https://docs.microsoft.com/azure/data-lake-store/data-lake-store-best-practices#performance-and-scale-considerations)<br>
* [Diagnose ADLS Gen1 throttling errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError/)<br>
* [Diagnose ADLS Gen1 timeout errors](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError/)<br>
