<properties
    pageTitle="Hyperscale (Citus) server is facing high CPU usage"
    description="Hyperscale (Citus) server is facing high CPU usage"
	infoBubbleText="Server is facing high CPU usage. See details on the right"
    service="microsoft.dbforpostgresql"
    resource="dbforpostgresql"
    authors="onlined"
    ms.author="ekdursun"
    displayOrder="100"
	articleId="dbforpostgresql-asc-citus-performance-highcpu"
	diagnosticScenario="OrcasBreadthCitusHighCPU"
    selfHelpType="rca"
    supportTopicIds="32639985,32639986,32639987,32640019,32640025,32640026,32640027"
    resourceTags="linux"
    productPesIds="16222,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforCitus"
/>

# Server is facing high CPU usage

<!--issueDescription-->
Your CPU percentage of your Hyperscale (Citus) server <!--$ServerName-->ServerName<!--/$ServerName--> is above 90% for more than 60 minutes between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->. High CPU percent could be due to multiple causes.
<!--/issueDescription-->

## **Recommended Steps**

* Review *CPU percent* in the Metrics window of the portal. If CPU spikes correlate with times when you increased your query workload, consider scaling up vCores to increase compute.
* Compare *Active Connections* and *CPU percent* side-by-side in the Metrics window. If your active connections increases correlate with CPU spikes, consider using a [connection pooler between your application and coordinator](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Not-all-Postgres-connection-pooling-is-equal/ba-p/825717). A pooler like [pgBouncer](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Steps-to-install-and-setup-PgBouncer-connection-pooling-proxy/ba-p/730555) would help optimize connection management.

## **Recommended Documents**

* [Query performance tuning on Citus](http://docs.citusdata.com/en/stable/performance/performance_tuning.html)
* [Using pg_stat_statements to extract insights](https://www.citusdata.com/blog/2019/02/08/the-most-useful-postgres-extension-pg-stat-statements/)
* [Monitoring overview document for Hyperscale (Citus)](https://docs.microsoft.com/azure/postgresql/concepts-hyperscale-monitoring).
* [Performance best practices for using Azure Database for PostgreSQL](https://azure.microsoft.com/blog/performance-best-practices-for-using-azure-database-for-postgresql/)<br>
* [Performance Troubleshooting Basics on Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Performance-Troubleshooting-Basics-on-Azure-Database-for/ba-p/819227) <br>
* [Performance troubleshooting using new Azure Database for PostgreSQL features](https://azure.microsoft.com/blog/performance-troubleshooting-using-new-azure-database-for-postgresql-features/)
* [Azure Database for PostgreSQL documentation](https://docs.microsoft.com/azure/postgresql/)
