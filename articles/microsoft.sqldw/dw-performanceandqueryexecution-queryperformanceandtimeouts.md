<properties
    pageTitle="Query performance and timeouts"
    description="Query performance and timeouts"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635214"
    productPesIds="15818"
    displayOrder="32"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-performanceandqueryexecution-queryperformanceandtimeouts.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Query performance and timeouts

## **Recommended Steps**

* Check [Analyze your workload in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) for queued query and the resources a request is waiting for
* Check [Sys.dm_pdw_errors](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-errors-transact-sql?view=azure-sqldw-latest) for errors
* If you experience slow query or load performance, ensure you have allocated enough memory. Check [Example code for finding the best resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#example-code-for-finding-the-best-resource-class).
* Internal DMS errors related to columnstore compression exceeding the remaining memory can be addressed by [increasing the resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class).

## **Recommended Documents**

* [Performance tuning with result set caching](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-result-set-caching)
* [Performance tuning with ordered clustered columnstore index](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-ordered-cci)
* [Performance tuning with materialized views](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-materialized-views)
* [Analyze your workload in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs)
* [Workload management with resource classes in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management)
