<properties
  pagetitle="Azure Database for MySQL ERROR 1040 (08004): Too many connections"
  description="Azure Database for MySQL ERROR 1040 (08004): Too many connections"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse, jtoland"
  selfhelptype="Generic"
  supporttopicids="32788637"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="c37ebf9e-2614-4ce3-b335-05d0283cbd96"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Azure Database for MySQL ERROR 1040 (08004): Too many connections

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* Review [Single server max connection limits](https://docs.microsoft.com/azure/mysql/concepts-server-parameters#max_connections) which covers the limit for each tier, and then increase value of the `max_connections` parameter accordingly. For the best experience, it is recommended to use a connection pooler such as ProxySQL to efficiently manage connections.
* If you are encountering connection failures or timeouts during peak hours, check your active connections and CPU/memory/IO usage percentage on the **Metrics** tab in the portal. Consider upgrading your server if any resource is hitting 100%. For more information, see [performance troubleshooting basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).
* If you see an unexpectedly high number of connections, check your application code and retry configuration as well.
* Verify that all connections are actually in use. Closing idle connections and ideally using connection pooling helps to optimize the number of concurrent connections.

## Quick tips

* Azure Database for MySQL Single Server has a fixed limit of maximum allowed concurrent connections. This limit depends on the compute resources provisioned for your server. For information about the current max number of connections, see  [Server parameters in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-server-parameters).
* To ensure healthy resource utilization, [Create a Monitoring Dashboard for Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/create-a-monitoring-dashboard-for-azure-database-for-mysql/ba-p/1233203).

## **Recommended Documents**

* [Azure Database for MySQL Single Server - Service limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
