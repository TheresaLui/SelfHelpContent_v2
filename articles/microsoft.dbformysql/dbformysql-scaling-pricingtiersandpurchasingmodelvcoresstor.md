<properties
    pageTitle="Pricing tiers and purchasing model in Azure Database for MySQL"
    description="Pricing tiers and purchasing model in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="andrela"
    ms.author="ajlam"
    displayOrder="190"
    selfHelpType="generic"
    supportTopicIds="32640085"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a7d92580-c82b-45ac-84bc-c44c799ac0a9"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Pricing tiers and purchasing model in Azure Database for MySQL

Azure Database for MySQL offers two deployment types - single server and flexible server. Server resources are managed using compute and storage.

*Single server*

Azure Database for MySQL Single Server resources are managed through compute and storage configurations. Refer to the [pricing tier documentation](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers) to learn more.

* Compute - single servers can be created in the following tiers:
  * **Basic** tier is designed for workloads requiring light compute and I/O performance (1-2 vCores)
  * **General Purpose** tier is for most business workloads requiring balanced compute and memory with scalable I/O throughput (2-64 vCores)
  * **Memory Optimized** tier is for high performance database workloads requiring in-memory performance for faster transaction processing and higher concurrency (2-32 vCores)
  * Please note that changing to and from the Basic pricing tier after server creation is not supported
* Storage
  * **Basic** tier can support up to 1 TB. IOPS are variable.
  * **General Purpose** and **Memory Optimized** tiers support scaled up to 16 TB. IOPS scale with storage in a 3 IOPS per GB ratio. Maximum 20,000 IOPS supported.

*Flexible server*

Azure Database for MySQL Flexible Server resources are managed through compute and storage configurations. Refer to the [compute and storage documentation](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage) to learn more.

* Compute - flexible servers can be created in the following compute tiers:
  * **Burstable** compute tier is designed for that don’t need the full CPU continuously (1-2 vCores)
  * **General Purpose** compute tier is for most business workloads requiring balanced compute and memory with scalable I/O throughput (2-64 vCores)
  * **Memory Optimized** compute tier is for high performance database workloads requiring in-memory performance for faster transaction processing and higher concurrency (2-64 vCores)
* Storage
  * All compute tiers support up to 16 TB
* IOPS
  * The minimum effective IOPS is 100 across all compute tiers & sizes
  * The max effective IOPS is determined by both compute and storage configurations

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)
