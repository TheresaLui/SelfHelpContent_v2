<properties
    pageTitle="Troubleshooting query insights performance insights in Azure Database for MySQL Single Server"
    description="Troubleshooting query insights performance insights in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="bahusse"
    displayOrder="250"
    selfHelpType="generic"
    supportTopicIds="32747578"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b54badaa-461e-4bd8-97f4-a2184a87d7a1"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshooting query performance in Azure Database for MySQL Single Server

Query performance issues can have many different root causes. Work through the following steps to resolve for the most common causes.

## **Recommended Steps**

**Troubleshooting slow query performance?**

Review your queries for any recent changes that might have caused the unexpected behavior. Also be sure to check the top consumers in terms of database usage. You can use [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to identify top consumers, and then use [Explain to profile and optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
For more information about how to resolve issues with query performance, see [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).

**Troubleshooting high CPU usage?**

If you are experiencing high usage on the CPU, remember that the number of active connections to your server can cause a spike. Be sure to review [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842). For more information about resolving issues related to high CPU usage, see [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

**Troubleshooting out of memory issues?**

If you are experiencing out of memory issues, see [Tune your server parameters](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters).

**Troubleshooting out of connections issues?**

If you are experiencing out of connections issues, see [Use connection pooling](https://docs.microsoft.com/azure/mysql/app-development-best-practices#use-connection-pooling).

**Is your database tuned for best application performance?** Consider [tuning your server parameters for best performance](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters).

**Use our intelligent performance features for additional insights:**

  1. [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store)
  2. [Query Performance Insights](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
  3. [Performance Recommendations](https://docs.microsoft.com/azure/mysql/concepts-performance-recommendations)

* If you want to use Query Store, make that **default_transaction_read_only** is not set to `ON`. Make sure that you have the right set of indexes created for your queries.
* Make sure that you don't hit the [limitations](https://docs.microsoft.com/azure/mysql/concepts-query-store#limitations-and-known-issues).

## **Recommended Documents**

*   [Query store documentation](https://docs.microsoft.com/azure/mysql/concepts-query-store)
*   [Query performance insights documentation](https://docs.microsoft.com/azure/mysql/concepts-query-performance-insight)
