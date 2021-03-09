<properties
  pagetitle="Troubleshooting query performance in Azure Database for MySQL&#xD;"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="pariks,bahusse"
  selfhelptype="Generic"
  supporttopicids="32747589"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="cb86db30-6635-4eb9-83b3-6274ccd90a0d"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Troubleshooting query performance in Azure Database for MySQL

### **Fix it yourself**

Query performance issues can have many different root causes. Most users can resolve common causes for performance issues by using the following information.

**Are you using a Basic Tier server?**

Basic Tier servers are intended for testing, development, and small-scale or infrequently used applications. Therefore, a production workload can max out resources easily. For more information, see [Understanding Performance in Basic Tier for Azure Database MySQL](https://techcommunity.microsoft.com/t5/azure-database-support-blog/understanding-performance-in-basic-tier-for-azure-database/ba-p/369142).

**Troubleshooting CPU high usage?**

See [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

Did you know that the number of active connections can cause a CPU spike? Make sure that you are [connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842).

**Is Azure MySQL running slower than usual?**

Analyzing your tables often pushes better execution plans for your queries. Consider [creating a dashboard for Azure Database for MySQL to monitor CPU, memory, and number of connections](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/create-a-monitoring-dashboard-for-azure-database-for-mysql/ba-p/1233203).

**Is your database tuned for best application performance?**

Consider [tuning your server parameters for best performance](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters).

**Want more advanced performance monitoring?**

See [sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema).

**Is a specific query slow?**

Consider using [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to spot slow queries and then [Explain and Optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
  - Make sure that you have the right set of indexes created for your queries.
  - Make sure that there are no deadlocks in concurrent queries.
  - Monitor the resource consumption of your server. If you max out I/O or compute resources, increase or scale up the resource on which you are limited.
  - Only retrieve the columns that you really need, instead of using `select \*`.

## **Recommended Documents**

* [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
* [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
* [Performance Recommendations](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)
* [Monitor and Tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring)
* [Best practices for building an application with Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/app-development-best-practices)
