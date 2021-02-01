<properties
  pagetitle="Error while scaling a resource in Azure Database for MySQL"
  description="Error while scaling a resource in Azure Database for MySQL"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="ajlam,jtoland"
  selfhelptype="Generic"
  supporttopicids="32640054"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="58f4750d-e3ae-4f4d-96c6-f0eb789ae5f7"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Error while scaling a resource in Azure Database for MySQL

Azure Database for MySQL Single server and Flexible server offer scaling for compute and storage resources. Scaling compute resources (across compute/pricing tiers or vCores) requires a server restart. Scaling storage is an online operation that does not require a server restart.

Most users can resolve their issues by considering the following points.

### Considerations

*Single server*

* Unable to scale from Basic to General Purpose/Memory Optimized service tiers, or vice versa.

  To switch from Basic to General Purpose or Memory Optimized, or vice versa, follow the steps in the blog post [Upgrade from Basic to General Purpose or Memory Optimized tiers](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404).

* Connections are dropped and no new connections can be established while vCores are scaled.

  vCore scaling requires a server restart. When new connections cannot be established, the time it takes the window to display varies, but in most cases, it takes under a minute. It is recommend to implement [retry logic](https://docs.microsoft.com/azure/mysql/concepts-connectivity) so that your application can seamlessly reconnect to the MySQL server after the scale operation is completed. Storage scaling does not require a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica.

  Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* Cannot scale up provisioned storage to 16 TB.

  Storage on a server that supports up to 4 TB cannot be increase. To move to a server with 16 TB of storage, create a new server using the 16 TB storage option and then perform a dump & restore to the new server.

*Flexible server*

* Connections are dropped and no new connections can be established while vCores are scaled.

  vCore scaling requires a server restart. When new connections cannot be established, the time it takes the window to display varies, but in most cases, it takes under a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server after the scale operation is completed. Storage scaling does not require a restart.

* Cannot scale up the master server when a replica exists, or cannot scale down a replica:

  * Before a master server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the master.

The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177)

## **Recommended Documents**

* [Azure Database for MySQL documentation](https://docs.microsoft.com/azure/mysql/)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Azure Database for MySQL Flexible Server - Compute + storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)<br>
* [Read Replicas in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-read-replicas#replica-configuration/)