<properties
    pageTitle="Specific errors or exceptions"
    description="Specific errors or exceptions"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635219"
    productPesIds="15818"
    displayOrder="31"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-performanceandqueryexecution-specificerrorsorexceptions.md"
    cloudEnvironments="public"
/>

# Specific errors or exceptions

## **Recommended Steps**

* Check [Analyze your workload in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) for queued query and the resources a request is waiting for.
* To resolve out of memory errors, [try increasing the user's resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class) or [scale your data warehouse to a larger service level](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-portal).
* To resolve syntax error for queries, check the [T-SQL syntax](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-reference-tsql-statements).

## **Recommended Documents**

* [Sys.dm_pdw_errors](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-errors-transact-sql?view=azure-sqldw-latest)
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)
