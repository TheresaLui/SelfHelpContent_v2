<properties
    pageTitle="Troubleshooting query performance in Azure Database for PostgreSQL"
    description="Troubleshooting query performance in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32640025"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public, Fairfax"
    articleId="4291a00c-8807-495e-909e-bbcf8a8b765f"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Troubleshooting query performance in Azure Database for PostgreSQL

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Recommended Steps**

* Use the intelligent performance features for additional insights:

  * [Query Store](https://docs.microsoft.com/azure/postgresql/concepts-query-store)
  * [Query Performance Insights](https://docs.microsoft.com/azure/postgresql/concepts-query-performance-insight)
  * [Performance Recommendations](https://docs.microsoft.com/azure/postgresql/concepts-performance-recommendations)

* Ensure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Connection latency can impact query performance. Check connection latency by timing how long a 'SELECT 1' takes.
* Monitor the resource consumption of your server. If compute, memory or IO is the limiting factor, consider scaling up the resource that you are limited on.
* Only retrieve the columns you really need instead of using 'SELECT *'
* Double-check your logging settings, including parameters like log_statement_stats, log_statement, log_min_duration_statement, and pg_stat_statements.track. High levels of logging impact performance.

## **Recommended Documents**

* [Monitor and tune](https://docs.microsoft.com/azure/postgresql/concepts-monitoring)
* [Performance checklist](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/azure-database-for-postgresql-checklist-for-performance/ba-p/1113378)
