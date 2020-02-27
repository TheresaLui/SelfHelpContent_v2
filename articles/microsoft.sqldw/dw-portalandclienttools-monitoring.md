<properties
    pageTitle="Using portal and client tools - Monitoring, metrics, and alerts"
    description="Using portal and client tools - Monitoring, metrics, and alerts"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635205"
    productPesIds="15818"
    displayOrder="61"
    selfHelpType="generic"
    resourceTags="datawarehouse"
    articleId="dw-portalandclienttools-monitoring.md"
    cloudEnvironments="public, Fairfax"
/>

# Monitoring, metrics or alerts

## **Recommended Steps**

* Monitoring resource utilization [from Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-concept-resource-utilization-query-activity):

  * When viewing resource utilization from the Azure portal, the metric aggregation occurs across all the compute nodes of the data warehouse. For data warehouses with a single compute node (DW500c and below), Max, Min, and Avg aggregation types will have the same values.
  * To determine the size of your data warehouse, use sp_spaceused. Portal storage size metrics such as data warehouse size, snapshots, and geo-backups are coming soon.
  * To determine data and log space information, see this [doc](https://docs.microsoft.com/sql/relational-databases/databases/display-data-and-log-space-information-for-a-database?view=sql-server-2017)
  * Failed and successful connections metrics are reported for a particular database/data warehouse - not for the logical server

* Monitoring resource utilization and query activity from [Dynamic Management Views (DMVs)](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor):

  * Most query informational DMVs have a [10,000 row limit](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-service-capacity-limits#metadata). The busier your workload, the sooner you will find yourself hitting this limit. 
  * DMVs are split into pass through DMVs and managed DMVs. Managed DMVs is like sys.dm_pdw_exec_requests which run on the control node and provide a uniform view and experience across the data warehouse. Pass through DMVs run on the compute nodes and  return the results from each node with additional columns for the distribution id and node id. When using these DMVs, make sure the DMV is of the form "sys.dm_pdw_nodes_*".

* Monitoring query activity [from Azure Portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-monitor-workload-portal) using Log Analytics for long term retention

## **Recommended Documents**

* [Manageability and monitoring](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-overview-manageability-monitoring)
* [Understanding metrics and logs available in the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-concept-resource-utilization-query-activity)
* Learn how to programmatically access metrics and query activity in the [portal](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-monitor-workload-portal) or [DMVs](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor)
