<properties
    pageTitle="Orcas MariaDB server is facing out of memory errors"
    description="Orcas MariaDB server is facing out of memory errors"
    infoBubbleText="Server is facing out of memory errors. See details on the right"
    service="microsoft.dbformariadb"
    resource="dbformariadb"
    authors="congwang"
    ms.author="conwan"
    displayOrder="100"
    articleId="dbformariadb-asc-performance-outofmemory"
    diagnosticScenario="OrcasMariaDBPerfOutofMemory"
    selfHelpType="rca"
    resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Server is facing out of memory errors

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> is facing Out of Memory errors from <!--$StartTime-->StartTime<!--/$StartTime--> to <!--$EndTime-->EndTime<!--/$EndTime--> (UTC).
<!--/issueDescription-->

## **Recommended Steps**

* Review *Memory percent* in the Metrics window of the portal. If memory spikes correlate with times when you increased your query workload, consider using higher SKU or choose Memory Optimized SKU.
* Consider reducing innodb_buffer_pool_size to release some memory for queries to allocate more
* Use the intelligent performance features for additional insights. For more information, review the [Monitoring overview](https://docs.microsoft.com/azure/mariadb/concepts-monitoring).

## **Recommended Documents**

* [Pricing tiers - Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers)<br>
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB) <br>
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
