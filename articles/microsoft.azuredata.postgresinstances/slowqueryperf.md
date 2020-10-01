<properties
  pagetitle="slowqueryperf"
  service="microsoft.azuredata"
  resource="postgresinstances"
  ms.author="pookam"
  selfhelptype="Generic"
  supporttopicids="32745092"
  productpesids="17124"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="0483e5b0-069f-49ac-adf8-6175e2ce29f7"
  ownershipid="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale" />
  
# Troubleshoot query execution problems in Azure Database for PostgreSQL

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service. Follow the recommended steps to troubleshoot your problem.

## **Recommended Steps**

* Review your queries for any changes that might have caused the unexpected behavior
* Monitor the resource consumption of your server using Grafana & Kibana Dashboards. If you max out either IO or compute resources, increase scale up the resource that you are limited on.
* Verify that you are experiencing slow query performance due to query execution itself you can prefix EXPLAIN ANALYZE in front of the query and look at the Execution time value
* Ensure you have the right set of indexes created for your queries
* Make sure that there are no deadlocks in the concurrent queries
* Only retrieve the columns you really need instead of using `SELECT *`
* Double-check your PostgreSQL logging settings (see below). Check if there was any schema changes, for example:
   * Whether an index was dropped
   * If you added columns, do you need a new index?
* Check if a significant proportion of the data was changed. If so, did you update the indexes?

## **Recommended Documents**

- [Useful Diagnostic Queries](http://docs.citusdata.com/en/v9.4/admin_guide/diagnostic_queries.html) 
- [Tuning your PostgreSQL Server](https://wiki.postgresql.org/wiki/Tuning_Your_PostgreSQL_Server) 
- [Using Postgres extensions](https://docs.microsoft.com/azure/azure-arc/data/using-extensions-in-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
