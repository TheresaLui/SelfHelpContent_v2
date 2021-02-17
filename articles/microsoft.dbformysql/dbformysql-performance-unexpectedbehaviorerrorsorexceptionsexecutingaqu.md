<properties
    pageTitle="Troubleshoot query execution problems in Azure Database for MySQL"
    description="Troubleshoot query execution problems in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="bahusse"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32640095"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="449f5c2d-d791-4b88-b7e1-78ccf5af4a01"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Troubleshoot query execution problems in Azure Database for MySQL

Query execution issues can be caused by the database engine itself or by the interaction of the database engine and the service. Use the following steps to troubleshoot your issue.

### Fix it yourself

**Troubleshooting timeouts or the loss of connectivity**

For information about how to resolve timeouts or connectivity issues, see [Troubleshoot issues connecting to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues). You may want to adjust application-side parameters such as `autoReconnect` and `keepAlive`. Also see [Handling transient errors](https://docs.microsoft.com/azure/mysql/concepts-connectivity#handling-transient-errors).

**Troubleshooting slow query performance**

Review your queries for any recent changes that might have caused the unexpected behavior. Also be sure to check the top consumers in terms of database usage. You can use [Query Store](https://docs.microsoft.com/azure/mysql/concepts-query-store) and [Slow Query log](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal) to identify top consumers, and then use [Explain to profile and optimize your query](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).
For more information about how to resolve issues with query performance, see [Troubleshoot query performance in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-query-performance).

**Troubleshooting high CPU usage**

If you are experiencing high usage the CPU, remember that the number of active connections to your server can cause a spike. Be sure to review [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842). For more information about resolving issues related to high CPU usage, see [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

**Troubleshooting out-of-memory issues**

If you are experiencing out-of-memory issues, see [Tune your server parameters](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters).

**Troubleshooting out-ofconnections issues**

If you are experiencing out-of-connections issues, see [Use connection pooling](https://docs.microsoft.com/azure/mysql/app-development-best-practices#use-connection-pooling).

**Is your database tuned for best application performance?** 

Consider [tuning your server parameters for best performance](https://docs.microsoft.com/azure/mysql/app-development-best-practices#tune-your-server-parameters).

**Using triggers or definers**

Consider using [`log_bin_trust_function_creators`](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#log_bin_trust_function_creators) and [Tips and Tricks for Azure Database for MySQL Super user errors](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912).

**Enabling or disabling global server parameter** 

Azure Database for MySQL exposes the ability to change the value of various MySQL server parameters using [the Azure portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters), [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-cli), and [PowerShell](https://docs.microsoft.com/azure/mysql/howto-configure-server-parameters-using-powershell), to match your workload's needs.

### Quick tips

Be sure to consider the following points:
- Monitor resource consumption on your server. If you max out either I/O or compute resources, scale up the resources that are limited. For more information, see [Monitoring in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-monitoring).
- Don’t forget to search the internet for potential solutions from the MySQL community.

## **Recommended documents**

- [How to use sys_schema views for performance tuning](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-sys-schema).
- [Monitor and tune](https://docs.microsoft.com/azure/mysql/concepts-monitoring/).
- [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/).
