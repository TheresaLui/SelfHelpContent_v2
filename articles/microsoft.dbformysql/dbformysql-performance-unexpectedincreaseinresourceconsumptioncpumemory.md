<properties
  pagetitle="Troubleshooting unexpected increase in resource consumption&#xD;"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="pariks,bahusse"
  selfhelptype="Generic"
  supporttopicids="32640096"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="64dc203f-500c-43b0-9096-2114c4910381"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Troubleshooting unexpected increase in resource consumption

Increase in resource consumption can be a result of an explicit user action or changes in the workload.

### **Fix it yourself**

* **Troubleshooting CPU high utilization?** <br>
Please take a look at the [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).
Did you know that the number of active connection can cause a CPU spike? Review ways to [connect efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842).

* **Have you checked the database utilization top consumers?** <br>
Consider using [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to spot top consumers of resources and waits, and then [Explain and Optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
    1. Ensure you have the right set of indexes created for your queries
    2. Make sure that there are no deadlocks in the concurrent queries
    3. Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase the resource that you are limited on.
    4. Only retrieve the columns you really need instead of using `select \*`

* **Do you feel Azure MySQL is running slower than usual?** <br>
Analyzing your tables frequently pushes better execution plans for your queries. Also consider [Creating CPU, Memory and number of connections Monitoring Dashboard for Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/create-a-monitoring-dashboard-for-azure-database-for-mysql/ba-p/1233203).

* **Are you using Basic Tier server?** <br>
Basic tier servers are intended for testing, development, or small-scale infrequently-used applications. Production workloads can max out resources easily. For more information read [Understanding Performance in Basic Tier for Azure Database MySQL](https://techcommunity.microsoft.com/t5/azure-database-support-blog/understanding-performance-in-basic-tier-for-azure-database/ba-p/369142).

**Quick tips**
* Adjust the pricing-tier or compute size in relation to the increase in the workload.
* You can increase the IOPS available to your server by scaling up storage. IOPS scale with the size of the provisioned storage in a 3:1 ratio.
* Ensure there are no changes to the pricing-tier or compute size of your service that might have triggered it.
* Check if there are any schema changes (for example, if an index was dropped)
* Ensure that the statistics are up to date

## **Recommended Documents**
* [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
* [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
* [Monitor and Tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring)
* [Best practices for building an application with Azure Database for MySQL]
* [Performance Recommendations in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)<br>
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)
