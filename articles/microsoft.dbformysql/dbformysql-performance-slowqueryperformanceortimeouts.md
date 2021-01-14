<properties
    pageTitle="Troubleshooting query performance in Azure Database for MySQL"
    description="Troubleshooting query performance in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="90"
    selfHelpType="generic"
    supportTopicIds="32640094"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="69a504ec-67e1-4d7a-ad2f-46ec95ca044a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting query performance in Azure Database for MySQL

Query performance issues can have many different root causes. Work through the recommended steps to solve for the most common causes for performance issues.

## **Fix it yourself**

* **Are you using Basic Tier server?** Please note that basic tier servers are intended for testing, development or small-scale infrequently used applications and production workload can max out resources easily. For more information read [Understanding Performance in Basic Tier for Azure Database MySQL](https://techcommunity.microsoft.com/t5/azure-database-support-blog/understanding-performance-in-basic-tier-for-azure-database/ba-p/369142)

* **Troubleshooting CPU high utilization?** Please take a look at the [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).
Did you know that the number of active connection can cause a CPU spike? Please consider [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842).

* **Do you feel Azure MySQL is running slower than usual?** Please note that analyzing your tables frequently pushes better execution plans for your queries. Also consider [Creating CPU, Memory and number of connections Monitoring Dashboard for Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/create-a-monitoring-dashboard-for-azure-database-for-mysql/ba-p/1233203).

* **Is your database tuned for best application performance?** Consider [Tuning your server parameters for best performance](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters)
* **Care for more advance Performance monitoring?** [sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)

* **Specific Query is slow?** Consider using [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to spot slow queries and then [Explain and Optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
    1. Ensure you have the right set of indexes created for your queries.
    2. Make sure that there are no deadlocks in the concurrent queries.
    3. Monitor the resource consumption of your server. If you max out either I/O or compute resources, increase scale up the resource that you are limited on.
    4. Only retrieve the columns you really need instead of using `select \*`.

## **Recommended Documents**
* [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
* [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
* [Performance Recommendations](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)
* [Monitor and Tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring)
* [Best practices for building an application with Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/app-development-best-practices)
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)