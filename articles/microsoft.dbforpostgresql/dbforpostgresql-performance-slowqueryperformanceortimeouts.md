<properties
    pageTitle="Troubleshooting query performance in Azure Database for PostgreSQL"
    description="Troubleshooting query performance in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32640025, 32781012"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4291a00c-8807-495e-909e-bbcf8a8b765f"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting query performance in Azure Database for PostgreSQL

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Recommended Steps**

### **Issue:** Slow query performance due to query execution issues

To verify that you are experiencing slow query performance due to query execution itself, you can prefix `EXPLAIN ANALYZE` in front of the query, and look at the `Execution time:` value.

* To improve performance, use the intelligent performance features for additional insights:

    * [Query Store](https://docs.microsoft.com/azure/postgresql/concepts-query-store)
    * [Query Performance Insights](https://docs.microsoft.com/azure/postgresql/concepts-query-performance-insight)
    * [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)

* Ensure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Monitor the resource consumption of your server:

    * Higher CPU Consumption: (a) check for high connection churn (open/close) as it can lead to high CPU consumption (b) check for long queries and look for ways to optimize them
    * IO throttling: Before opting to increase IOPS, identify queries that are generating most IOs and look for ways to reduce IO. For example, index may be missing.
    * High memory utilization: high memory can cause data churn leading to higher IOs
    * After evaluating your application, if you are still hitting the resource limits, consider scaling the required resource

* Only retrieve the columns you really need instead of using 'SELECT *'
* When loading large number of rows, try to batch them into transactions
* Double-check your PostgreSQL logging settings (see below)

### **Issue:** High connection latency (slow SELECT 1)

To verify this issue, open up a client that shows timing data (e.g. psql with `\timing` enabled), and run `SELECT 1`. This will show you the roundtrip latency of a basic query. This should be very fast (< 10 ms) if you are running in a VM that is located close to your database.

If this is higher than 10 ms, your performance issues are likely due to the network latency, and not due to any other issues. We recommend running your application in the same region as your database.

### **Issue:** High levels of logging impacting performance

With certain configurations, your PostgreSQL database server outputs a high amount of log lines. This can cause the whole server to slow down, including causing queries to be slow. We recommend that you test with the following log configuration settings, and then verify whether this improves performance:

* `debug_print_parse = OFF`
* `debug_print_plan = OFF`
* `debug_print_rewritten = OFF`
* `log_duration = OFF`
* `log_min_duration_statement = -1`
* `log_statement_stats = OFF`
* `log_statement = NONE`
* `pg_stat_statements.track = NONE`

Additionally, you can consider setting `logging_collector = OFF`. This will only send the logs to Azure Monitor, and avoid storing them locally on the server. You may also want to tune server parameters `max_wal_size`, `checkpoint_completion_target` or `maintenance_work_mem` but these are very workload sensitive. For most workloads, the default configuration setting works.

## **Recommended Documents**

* [Monitor and tune](https://docs.microsoft.com/azure/postgresql/concepts-monitoring)
* [Performance checklist](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/azure-database-for-postgresql-checklist-for-performance/ba-p/1113378)
