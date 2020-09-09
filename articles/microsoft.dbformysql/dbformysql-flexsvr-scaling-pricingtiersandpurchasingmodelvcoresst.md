<properties
    pageTitle="Compute tiers and purchasing model in Azure Database for MySQL Flexible Server"
    description="Compute tiers and purchasing model in Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="360"
    selfHelpType="generic"
    supportTopicIds="32747630"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5b9c3a25-59c7-4b90-b76b-32980f09a094"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Compute tiers and purchasing model in Azure Database for MySQL Flexible Server

Azure Database for MySQL Flexible Server resources are managed through compute and storage configurations. Refer to the [compute and storage documentation](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage) to learn more.

*Compute*

Flexible servers can be created in the following compute tiers:

* **Burstable** compute tier is designed for that don’t need the full CPU continuously (1-2 vCores)
 * **General Purpose** compute tier is for most business workloads requiring balanced compute and memory with scalable I/O throughput (2-64 vCores)
 * **Memory Optimized** compute tier is for high performance database workloads requiring in-memory performance for faster transaction processing and higher concurrency (2-64 vCores)

*Storage*

* All compute tiers support up to 16 TB

*IOPS*

 * The minimum effective IOPS is 100 across all compute tiers & sizes
 * The max effective IOPS is determined by both compute and storage configurations

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)<br>
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)