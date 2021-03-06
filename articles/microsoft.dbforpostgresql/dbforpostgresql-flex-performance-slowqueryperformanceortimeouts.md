<properties
    pageTitle="Troubleshooting query performance in Azure Database for PostgreSQL"
    description="Troubleshooting query performance in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32781011"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-performance-slowqueryperformanceortimeouts"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting query performance in Azure Database for PostgreSQL

Query performance issues can have many different root causes. To resolve the most common causes for performance issues, work through the following recommended steps.

## **Recommended Steps**

Issue: **Slow query performance due to query execution issues**

To verify that you are experiencing slow query performance due to query execution itself, prefix `EXPLAIN ANALYZE` in front of the query, and look at the `Execution time:` value.

* Ensure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Monitor the resource consumption of your server:

    * Higher CPU Consumption: (a) check for high connection churn (open/close) because it can lead to high CPU consumption, and (b) check for queries that are consuming the most CPUs and look for ways to optimize them
    * IO throttling: Before opting to increase IOPS, identify queries that are generating the most IOs and look for ways to reduce IO. For example, index may be missing.
    * High memory utilization: high memory can cause data churn leading to higher IOs
    * After evaluating your application, if you are still reaching the resource limits, consider scaling the required resource

* Only retrieve the columns you that really need instead of using 'SELECT *'
* Double-check your PostgreSQL logging settings (see additional details below)

Issue: **High connection latency (slow SELECT 1)**

To verify this issue, open up a client that shows timing data (for example, `psql` with `\timing` enabled), and run `SELECT 1`. This will show you the roundtrip latency of a basic query. This should be very fast (< 10 ms) if you are running in a VM that is located close to your database.

If this is higher than 10 ms, your performance issues are likely due to network latency and do not involve any other issues. We recommend running your application in the same region as your database.

Issue: **High levels of logging impacting performance**

With certain configurations, your PostgreSQL database server outputs a high amount of log lines. This can cause the whole server to slow down, including causing queries to be slow. We recommend testing with the following log configuration settings, and then verifying whether this improves performance:

* `debug_print_parse = OFF`
* `debug_print_plan = OFF`
* `debug_print_rewritten = OFF`
* `log_duration = OFF`
* `log_min_duration_statement = -1`
* `log_statement_stats = OFF`
* `log_statement = NONE`


Issue: **The Query Store, Query Performance Insights, Performance Recommendations** 

The Query Store, Query Performance Insights, and Performance Recommendations features are not currently supported on Flexible Server.
