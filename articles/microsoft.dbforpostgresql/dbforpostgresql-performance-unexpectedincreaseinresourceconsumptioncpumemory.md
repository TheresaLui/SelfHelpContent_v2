<properties
    pageTitle="Troubleshooting unexpected increase in resource consumption"
    description="Troubleshooting unexpected increase in resource consumption"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="100"
    selfHelpType="generic"
    supportTopicIds="32640027, 32781016"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3f47468a-cc1e-41c2-9665-57b66bbe16e2"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload. Increased CPU usage can also be caused by an issue with PostgreSQL internal processes, such as autovacuum not running as expected, or an unexpected increase in short-lived connections. For example, if you open large number of connections at the same time, you will see performance slowdown.

## **Recommended Steps**

* Ensure that there are no changes to the pricing tier of your service that might have triggered the increase
* Adjust the pricing tier commensurate to the increase in the workload
* Check if there are any schema changes, for example whether an index was dropped
* Ensure that the table statistics are up to date
* Determine when your tables were last vacuumed and tune threshold parameters (see **Recommended Documents** section)
* Check if there is a spike in short-lived connections
* Check if there is a spike in new connection requests
* Enable Query Store to see any changes in the workload or query regression. Refer to [Performance Troubleshooting with Query Store](https://azure.microsoft.com/blog/performance-troubleshooting-using-new-azure-database-for-postgresql-features/)

## **Recommended Documents**

* [Performance Recommendations in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)
* [Optimize autovacuum on Azure Database for PostgreSQL - Single Server](https://docs.microsoft.com/azure/postgresql/howto-optimize-autovacuum)
