<properties
  pagetitle="Scaling Azure Database for MySQL servers&#xD;"
  description="Scaling Azure Database for MySQL servers"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="ajlam,jtoland"
  selfhelptype="Generic"
  supporttopicids="32640086"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="d980b014-1500-4f79-a025-03717b4576da"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Scaling Azure Database for MySQL servers

In Azure Database for MySQL, you can scale both compute and storage resources. You can initiate scaling operations from the Azure portal, the Azure CLI, ARM templates, or the REST API.

Most users are able to resolve their issues by considering the following points.

### Considerations for Compute

* **Single server supports:**
  * Basic, General Purpose, and Memory Optimized pricing tiers
  * Scaling between the General Purpose and Memory Optimized tiers
  
  Scaling to/from the Basic tier isn't supported. To switch from the Basic to the General Purpose or Memory Optimized tier, or vice-versa, follow the steps in the blog post [Upgrade from Basic to General Purpose or Memory Optimized tiers](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404).

* **Flexible server supports:**
  * Burstable, General Purpose, and Memory Optimized compute tiers
  * Scaling between all compute tiers and sizes

* **Connections are dropped and no new connections can be established while scaling compute resources.**

  Compute scaling requires a server restart. When new connections can't be established, the time it takes for the window to appear varies, but in most cases, is under a minute. It is recommended to implement retry logic so that your application can seamlessly reconnect to the MySQL server after the scale operation is completed.

### Considerations for Storage

In both single and flexible server, scaling storage is an online operation that does not require a server restart.

* **Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later".** 
  
  Try to scale the server again after a few minutes have elapsed.

* **Single server**
  * The Basic tier can support up to 1 TB, with variable IOPS
  * The General Purpose and Memory Optimized tiers support scaling up to 16 TB. IOPS scale with storage in a ratio of three IOPS per GB, up to a maximum 20,000 IOPS

* **Flexible server**
  All compute tiers support up to 16 TB.


### Considerations for IOPS

* **Single server**
  * For the Basic tier, IOPS are variable
  * For the General Purpose and Memory Optimized tiers, IOPS scale with storage in a ratio of three IOPS per GB, up to a maximum of 20,000 IOPS

* **Flexible server**
  * The minimum effective IOPS is 100 across all compute tiers and sizes
  * The maximum effective IOPS is determined by both compute and storage configurations

### Considerations for Read replicas

* **Can't scale up the source server when a replica exists, or can't scale down a replica.**
  Before updating the configuration of a source server, update the configuration of the replica to equal or greater values. This action ensures that the replica can keep up with any changes made to the source.

Azure Database for MySQL does not support the Azure Monitor auto-scale feature. However, you can configure auto-scaling using Azure run books and Python. Refer to the blog post [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal)
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)
