<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for MySQL Single Server"
    description="Troubleshoot query execution problems in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="260"
    selfHelpType="generic"
    supportTopicIds="32747590"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d0b40449-51f6-465f-9c5c-9c80b12a20c7"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshoot query execution problems in Azure Database for MySQL Single Server

Query execution problems can be caused by the database engine itself or by the interaction of the database engine and the service.

To resolve query execution problems when working with Azure Database for MySQL Single Server, consider the following guidance.

## Fix it yourself

* **Troubleshooting timeouts or the loss of connectivity?**

  For information about how to resolve timeouts or connectivity issues, see [Troubleshoot issues connecting to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues).
* **Troubleshooting slow query performance?**

  Review your queries for any recent changes that might have caused the unexpected behavior. Also be sure to check the top consumers in terms of database utilization. You can use [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to identify top consumers, and then [use Explain to profile and optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).

  For more information about how to resolve issues with query performance, see [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
* **Troubleshooting high CPU utilization?**

  If you're experiencing high utilization on the CPU, remember that the number of active connections to your server can cause a spike. Be sure to review [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842). For more information about resolving issues related to high CPU utilization, see [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815)

* **Troubleshooting out of memory issues?**

  If you're experiencing out-of-memory issues, see [Tune your server parameters](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters) in the article on App development best practices.

* **Troubleshooting out of connections issues?**

  If you're experiencing out of connections issues, see [Use connection pooling](https://docs.microsoft.com/azure/mysql/app-development-best-practices#use-connection-pooling) in the article on App development best practices.

## Quick tips

Also, make sure to consider the following points.

* Monitor resource consumption on your server. If you max out either I/O or compute resources, scale up the resources that are limited. For more information, see [Monitoring in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-monitoring).
* Don’t forget to search for potential solutions from the MySQL community.

## **Recommended documents**

* [How to use sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema)
* [Monitor and tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring/)
* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql).
