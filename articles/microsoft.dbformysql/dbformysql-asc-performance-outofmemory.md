<properties
    pageTitle="Orcas MySQL server is facing out of memory errors"
    description="Orcas MySQL server is facing out of memory errors"
    infoBubbleText="Server is facing out of memory errors. See details on the right"
    service="microsoft.dbformysql"
    resource="dbformysql"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformysql-asc-performance-outofmemory"
    diagnosticScenario="OrcasMySQLPerfOutofMemory"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Server is facing out of memory errors

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> is facing Out of Memory errors from <!--$StartTime-->StartTime<!--/$StartTime--> to <!--$EndTime-->EndTime<!--/$EndTime--> (UTC).
<!--/issueDescription-->

## **Recommended Steps**

* Review *Memory percent* in the Metrics window of the portal. If memory spikes correlate with times when you increased your query workload, consider using higher SKU or choose Memory Optimized SKU.
* Consider reducing innodb_buffer_pool_size to release some memory for queries to allocate more
* Use the intelligent performance features for additional insights. For more information, visit the [Monitoring overview](https://docs.microsoft.com/azure/mysql/concepts-monitoring).

## **Recommended Documents**

* [Pricing tiers - Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL) <br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
