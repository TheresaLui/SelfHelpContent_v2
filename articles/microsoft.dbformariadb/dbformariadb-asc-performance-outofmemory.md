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
    cloudEnvironments="public"
/>

# Server is facing out of memory errors

<!--issueDescription-->
During our investigation we found that your server <!--$ServerName-->ServerName<!--/$ServerName--> has total <!--$Count-->Count<!--/$Count--> Out of Memory errors from <!--$StartTime-->StartTime<!--/$StartTime--> to <!--$EndTime-->EndTime<!--/$EndTime-->.
<!--/issueDescription-->

## **Recommended Steps**

* Review *Memory percent* in the Metrics window of the portal. If Memory spikes correlate with times when you increased your query workload, consider scaling up vCores to increase memory.
* Consider reducing innodb_buffer_pool_size to release some memory for queries to allocate more.
* Use the intelligent performance features for additional insights. For more information, visit the  [Monitoring overview document](https://docs.microsoft.com/azure/mariadb/concepts-monitoring)

## **Recommended Documents**

* [Pricing tiers - Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers)<br>
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMariaDB) <br>
* [Azure Database for MariaDB documentation](https://docs.microsoft.com/azure/mariadb/)
