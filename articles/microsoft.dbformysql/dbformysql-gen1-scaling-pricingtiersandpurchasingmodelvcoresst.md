<properties
    pageTitle="Pricing tiers and purchasing model in Azure Database for MySQL Single Server"
    description="Pricing tiers and purchasing model in Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="370"
    selfHelpType="generic"
    supportTopicIds="32747577"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9573f887-1924-41cd-aea2-c5de583ae929"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Pricing tiers and purchasing model in Azure Database for MySQL Single Server

Azure Database for MySQL Single Server resources are managed through compute and storage configurations. Refer to the [pricing tier documentation](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers) to learn more.

*Compute*

Single servers can be created in the following tiers:

 * **Basic** tier is designed for workloads requiring light compute and I/O performance (1-2 vCores)
 * **General Purpose** tier is for most business workloads requiring balanced compute and memory with scalable I/O throughput (2-64 vCores)
 * **Memory Optimized** tier is for high performance database workloads requiring in-memory performance for faster transaction processing and higher concurrency (2-32 vCores)
 * Please note that changing to and from the Basic pricing tier after server creation is not supported

*Storage*

 * **Basic** tier can support up to 1 TB. IOPS are variable.
 * **General Purpose** and **Memory Optimized** tiers support scaled up to 16 TB. IOPS scale with storage in a 3 IOPS per GB ratio. Maximum 20,000 IOPS supported.

## **Recommended Documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)<br>
* [Azure Database for MySQL Single Server - Pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)