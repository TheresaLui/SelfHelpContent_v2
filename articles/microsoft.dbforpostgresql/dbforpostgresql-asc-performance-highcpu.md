<properties
    pageTitle="PostgreSQL server is facing high CPU usage"
    description="PostgreSQL server is facing high CPU usage"
	infoBubbleText="Server is facing high CPU usage. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="danielcarbajal"
    ms.author="dacarbaj"
    displayOrder="100"
	articleId="dbforpostgresql-asc-performance-highcpu"
	diagnosticScenario="OrcasPostgresHighCPU"
    selfHelpType="rca"
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027, 32781006, 32781008, 32781010, 32781012, 32781014"
    resourceTags="windows, linux"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Server is facing high CPU usage

<!--issueDescription-->
We've detected that CPU percent is above 90% for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC) on PostgreSQL server <!--$ServerName-->ServerName<!--/$ServerName-->.
<!--/issueDescription-->

## **Recommended Steps**

* Review the *CPU percent* metric for your server. If CPU spikes correlate with times when you increased your query workload, consider scaling up vCores to increase compute.
* Compare *Active Connections* and *CPU percent* side-by-side in the Metrics window. If your active connections increases correlate with CPU spikes, consider using a [connection pooler between your application and Postgres server](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Not-all-Postgres-connection-pooling-is-equal/ba-p/825717). A pooler like [pgBouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555) would help optimize connection management.
* Use the Intelligent Performance features for additional insights into your queries. For more information, visit the [Monitoring overview document](https://docs.microsoft.com/azure/postgresql/concepts-monitoring).

## **Recommended Documents**

* [Performance best practices for using Azure Database for PostgreSQL](https://azure.microsoft.com/blog/performance-best-practices-for-using-azure-database-for-postgresql/)<br>
* [Performance Troubleshooting Basics on Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Performance-Troubleshooting-Basics-on-Azure-Database-for/ba-p/819227) <br>
* [Performance troubleshooting using new Azure Database for PostgreSQL features](https://azure.microsoft.com/blog/performance-troubleshooting-using-new-azure-database-for-postgresql-features/)
* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)
