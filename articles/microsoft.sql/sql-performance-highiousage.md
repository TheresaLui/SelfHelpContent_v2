<properties
    pageTitle="query execution/high IO usage"
    description="query execution/high IO usage"
    infoBubbleText="High IO usage detected. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="HiIOUsageIssue_3EE4845D-971B-4A4B-9D1E-64D8C0B54ABB"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749515, 32749520"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# High IO Usage Detected

<!--issueDescription-->
We ran diagnostics and detected high IO usage on database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->**. In the past 24 hours, there were **<!--$numOccurrences-->numOccurrences<!--/$numOccurrences-->** intervals of 5-minutes when the average IO usage was greater than 90%. When IO usage is high, your applications may experience performance issues like timeouts or increased latency.
<!--/issueDescription-->

## **Recommended Steps**

To reduce the IO usage on your database, follow these recommendations:

* Increase your IO capacity by upgrading your database compute size or service tier. See [vCore and DTU Purchasing Models](https://docs.microsoft.com/azure/azure-sql/database/purchasing-models) for more information.
* Identify and tune the queries consuming the most IO. See [Identify IO Performance Issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-io-performance-issues) for more information.
* To consolidate IO costs, group separate transactions into batches. See [Batching for Performance Improvements](https://docs.microsoft.com/azure/azure-sql/performance-improve-use-batching) for more information.

## **Recommended Documents**

* [Monitoring and Performance Tuning in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/monitor-tune-overview)
