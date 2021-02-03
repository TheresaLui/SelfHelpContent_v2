<properties
    pageTitle="Scaling Azure Database for MySQL servers"
    description="Scaling Azure Database for MySQL servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="andrela"
    ms.author="ajlam"
    displayOrder="180"
    selfHelpType="generic"
    supportTopicIds="32640086"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d980b014-1500-4f79-a025-03717b4576da"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Scaling Azure Database for MySQL servers

In Azure Database for MySQL, scaling can be done for both compute and storage resources. Scaling operations can be done from the Azure portal, Azure CLI, ARM templates, or REST API.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

*Compute*

* Single server
  * Supports Basic, General Purpose, and Memory Optimized pricing tiers
  * Scaling between General Purpose and Memory Optimized tiers is supported. Scaling to/from the Basic tier is not supported.
  * If you want to switch from Basic to General Purpose or Memory Optimized and vice-versa, please follow the steps in [Upgrade from Basic to General Purpose or Memory Optimized tiers](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Upgrade-from-Basic-to-General-Purpose-or-Memory-Optimized-tiers/ba-p/830404) blog

* Flexible server
  * Supports Burstable, General Purpose, and Memory Optimized compute tiers
  * Scaling between all compute tiers and sizes is supported

* Connections are dropped and no new connections can be established while scaling compute resources:
  * Compute scaling requires a server restart. The window when new connections cannot be established varies, but in most cases, is less than a minute. We recommend you implement retry logic so your application can seamlessly reconnect to the MySQL server once the scale operation is completed.

*Storage*

* In both single and flexible server, scaling storage is an online operation and does not require a server restart
* Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later". 
  * Try to scale the server again after a few minutes have passed.
* Single server
  * **Basic** tier can support up to 1 TB. IOPS are variable
  * **General Purpose** and **Memory Optimized** tiers support scaled up to 16 TB. IOPS scale with storage in a 3 IOPS per GB ratio. Maximum 20,000 IOPS supported.
* Flexible server
  * All compute tiers support up to 16 TB

*IOPS*

* Single server
  * **Basic** tier: IOPS are variable
  * **General Purpose** and **Memory Optimized** tiers: IOPS scale with storage in a 3 IOPS per GB ratio. Maximum 20,000 IOPS supported.

* Flexible server
  * The minimum effective IOPS is 100 across all compute tiers & sizes
  * The max effective IOPS is determined by both compute and storage configurations

*Read replicas*

* Cannot scale up the source server when a replica exists, or cannot scale down a replica. Before a source server configuration is updated to new values, update the replica configuration to equal or greater values. This action ensures the replica can keep up with any changes made to the source.

The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure runbook and Python. Please refer to [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)<br>
* [Manage Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal)<br>
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)<br>
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)